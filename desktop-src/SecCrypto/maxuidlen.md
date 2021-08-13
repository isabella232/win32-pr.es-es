---
description: Constante numérica que especifica el número máximo de caracteres que algunos de los proveedores criptográficos de Microsoft usarán al obtener el identificador de usuario.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a2cad5f6e676fc0e0677ccc9f76262f4ba4104aa58d0662b92f23206cb6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408015"
---
# <a name="maxuidlen"></a>MAXUIDLEN

MAXUIDLEN es una constante numérica que especifica el número máximo de caracteres que algunos de los proveedores criptográficos de Microsoft usarán al obtener el id. de usuario. MAXUIDLEN se define en Wincrypt.h.



| Constante o valor                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt> </dl> | Cuando el *parámetro pszContainer* de la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) es **NULL,** algunos de los proveedores criptográficos de Microsoft usan el nombre de inicio de sesión del usuario que ha iniciado sesión actualmente como nombre del contenedor de claves. MAXUIDLEN especifica el número máximo de caracteres, incluido el carácter **NULL** final, que estos proveedores usarán para el nombre de usuario.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




