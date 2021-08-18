---
description: La propiedad DVDAdm.DefaultSubpictureLCID establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para la secuencia de subpicture.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propiedad DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc67be112349a050df45f625fda6488c91b22dee357c820724de5842c156894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952994"
---
# <a name="defaultsubpicturelcid-property"></a>Propiedad DefaultSubpictureLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario `DVDAdm.DefaultSubpictureLCID` para el flujo de subpicture.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor Entero que representa el LCID de subpicture predeterminado especificado por el usuario tal como se almacena en la configuración del Registro para la aplicación de DVD. Este valor no es necesariamente el mismo que el flujo de subpicture predeterminado que se edtó en el DVD. Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de plataforma.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Si no se especifica ningún LCID de subimagen predeterminado, el objeto MSDVDAdm reproducirá la secuencia de subimagen marcada como la secuencia predeterminada en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



