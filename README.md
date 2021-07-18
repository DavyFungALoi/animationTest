# animationTest



function template(i, duration) {
    return `
        &:nth-child(${i + 1}) {
          transition-delay: ${`calc(${duration} * ${i + 3})`};
         }
      `;
}
function getAnimations() {
    let str = '';
    for (let index = 0; index < 4; index += 1) {
        str += template(index, index)
    }
    return str;
}
export const NavigationItem = styled.li`
${getAnimations()}
`;


https://spectrum.chat/styled-components/general/loop-nth-child-in-styled-component~7342bb0f-0fb6-4548-ac56-75834008af69

