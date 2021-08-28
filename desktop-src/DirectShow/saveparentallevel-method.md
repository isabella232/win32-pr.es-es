---
description: El método DVDAdm.SaveParentalLevel guarda un nuevo nivel parental predeterminado en el registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e372563a6f5a1fe8e893efeb86633baa6a03a7b72c79e3f05a3ec7372bec2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315955"
---
# <a name="saveparentallevel-method"></a>SaveParentalLevel (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El **método DVDAdm.SaveParentalLevel** guarda un nuevo nivel parental predeterminado en el registro.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica el nivel parental como valor anInteger de 1 a 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el nombre de usuario como string. (Actualmente se omite).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método permite a un usuario que conoce la contraseña actual guardar una nueva configuración de nivel parental en el registro. Al igual que con todos los **métodos de MSDVDAdm,** este método no afecta al nivel actual del reproductor; solo cambia la configuración del Registro, por lo que la próxima vez que se inicia el objeto MSWebDVD, se abrirá con el nuevo nivel. Especifique -1 para deshabilitar la administración parental. Para cambiar el nivel parental en el reproductor, llame a [**SelectParentalLevel**](selectparentallevel-method.md), que no cambia la configuración del Registro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




