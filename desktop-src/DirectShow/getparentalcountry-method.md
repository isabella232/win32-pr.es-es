---
description: El método DVDAdm.GetParentalCountry recupera el país o región parental que se guardó por última vez en el registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061119"
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

## <a name="remarks"></a>Observaciones

El país o región parental que recupera este método no es necesariamente el mismo país o región almacenado actualmente en el objeto MSWebDVD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




