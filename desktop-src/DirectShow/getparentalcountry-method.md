---
description: El método DVDAdm.GetParentalCountry recupera el país o región parental que se guardó por última vez en el registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756765"
---
# <a name="getparentalcountry-method"></a>Método GetParentalCountry

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.GetParentalCountry` método recupera el país o región parental que se guardó por última vez en el registro.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un entero que indica el código de país o región predeterminado almacenado en el Registro.

## <a name="remarks"></a>Comentarios

El país o región parental que recupera este método no es necesariamente el mismo país o región almacenado actualmente en el objeto MSWebDVD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




