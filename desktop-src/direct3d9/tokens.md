---
description: Los tokens se escriben como WORD little-endian. La siguiente lista de valores de token se divide en tokens independientes y de registro.
ms.assetid: vs|directx_sdk|~\tokens.htm
title: Tokens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf3e3654d90566fa6c4a6208c965518ce54acd3dd31669038de1b9a8ab38684d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095585"
---
# <a name="tokens"></a>Tokens

Los tokens se escriben como WORD little-endian. La siguiente lista de valores de token se divide en tokens independientes y de registro.

Los tokens de registro se definen como se muestra a continuación.


```
#define TOKEN_NAME         1
#define TOKEN_STRING       2
#define TOKEN_INTEGER      3
#define TOKEN_GUID         5
#define TOKEN_INTEGER_LIST 6
#define TOKEN_FLOAT_LIST   7
```



Los tokens independientes se definen como se muestra a continuación.


```
#define TOKEN_OBRACE      10
#define TOKEN_CBRACE      11
#define TOKEN_OPAREN      12
#define TOKEN_CPAREN      13
#define TOKEN_OBRACKET    14
#define TOKEN_CBRACKET    15
#define TOKEN_OANGLE      16
#define TOKEN_CANGLE      17
#define TOKEN_DOT         18
#define TOKEN_COMMA       19
#define TOKEN_SEMICOLON   20
#define TOKEN_TEMPLATE    31
#define TOKEN_WORD        40
#define TOKEN_DWORD       41
#define TOKEN_FLOAT       42
#define TOKEN_DOUBLE      43
#define TOKEN_CHAR        44
#define TOKEN_UCHAR       45
#define TOKEN_SWORD       46
#define TOKEN_SDWORD      47
#define TOKEN_VOID        48
#define TOKEN_LPSTR       49
#define TOKEN_UNICODE     50
#define TOKEN_CSTRING     51
#define TOKEN_ARRAY       52
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 



