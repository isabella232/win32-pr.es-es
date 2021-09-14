---
title: Interfaz IWMPSettings (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos que obtienen o establecen los valores de Reproductor de Windows Media configuración. La interfaz IWMPSettings expone las siguientes propiedades.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- Interfaz IWMPSettings (VB y C) Reproductor de Windows Media
- Interfaz IWMPSettings (VB y C) Reproductor de Windows Media , descrita
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db911cc6d18ba40777e77a803480c7fcab4ff8ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241749"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interfaz IWMPSettings (VB y C#)

Proporciona propiedades y métodos que obtienen o establecen los valores de Reproductor de Windows Media configuración.

La **interfaz IWMPSettings** expone las siguientes propiedades.

## <a name="members"></a>Members

La **interfaz IWMPSettings (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPSettings (VB y C#)** tiene estos métodos.



| Método                                                               | Descripción                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Devuelve un valor que indica si el modo de bucle o el modo aleatorio están activos.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Establece el modo de bucle o el modo aleatorio en activo o inactivo.<br/>               |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPSettings (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                              | Tipo de acceso           | Descripción                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autostart**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente. <br/>                                     |
| [**equilibrar**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lectura y escritura<br/> | Obtiene o establece el equilibrio estéreo actual.<br/>                                                                                          |
| [**Baseurl**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lectura y escritura<br/> | Obtiene o establece la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL insertados en contenido multimedia digital. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lectura y escritura<br/> | Obtiene o establece el nombre del marco utilizado para mostrar una dirección URL que se recibe en un **evento scriptCommand.** <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lectura y escritura<br/> | Obtiene o establece un valor que indica si los cuadros de diálogo de error se muestran automáticamente.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador web. <br/>                                                  |
| [**Isavailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Solo lectura<br/>  | Obtiene un valor que indica si se puede realizar una acción especificada. En C#, este es el **método \_ get isAvailable.**<br/>             |
| [**Mudo**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lectura y escritura<br/> | Obtiene o establece un valor que indica si el audio está silenciado. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece el número de veces que se reproducirá un elemento multimedia. <br/>                                                                         |
| [**Tasa**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lectura y escritura<br/> | Obtiene o establece la velocidad de reproducción actual del vídeo. <br/>                                                                                |
| [**Volumen**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lectura y escritura<br/> | Obtiene o establece el volumen de reproducción actual. <br/>                                                                                        |



 

Obtenga una **interfaz IWMPSettings** mediante la siguiente propiedad.



| Object                                                                   | Propiedad                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Configuración**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





