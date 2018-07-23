# loDashes

Stuff I need to remember is better with a dash of loDash:

lodash helps simplify code by handling the null checking.., defaulting to false here is unnecessary 
but I think it helps clue the next developer to the intention of boolean.

        if (payload) {
            if (payload.hasOwnProperty('isFlexBuilder')) {
                isFlexBuilder = payload.isFlexBuilder;
            }
        }
        
        is better as
        
        isFlexBuilder = _.get(payload, 'isFlexBuilder', false);
