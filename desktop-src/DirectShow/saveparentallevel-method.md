---
description: El método DVDAdm. SaveParentalLevel guarda un nuevo nivel de parental predeterminado en el registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680300"
---
# <a name="saveparentallevel-method"></a>Método SaveParentalLevel

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método **DVDAdm. SaveParentalLevel** guarda un nuevo nivel de parental predeterminado en el registro.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica el nivel de parental como valor de entero de 1 a 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de usuario como una cadena. (Actualmente omitido).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método permite a un usuario que conoce la contraseña actual guardar una nueva configuración de nivel parental en el registro. Al igual que con todos los métodos de **MSDVDAdm**, este método no afecta al nivel actual del reproductor; solo cambia la configuración del registro, de modo que la próxima vez que se inicie el objeto MSWebDVD, se abrirá con el nuevo nivel. Especifique-1 para deshabilitar la administración parental. Para cambiar el nivel parental en el reproductor, llame a [**SelectParentalLevel**](selectparentallevel-method.md), que no cambia la configuración del registro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




