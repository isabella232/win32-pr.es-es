---
title: Interfaz IWMPSettings (VB y C) (WMP. h)
description: Proporciona propiedades y métodos que obtienen o establecen los valores de configuración de Windows Media Player. La interfaz IWMPSettings expone las siguientes propiedades.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- IWMPSettings (VB y C) interfaz de Windows Media Player
- IWMPSettings (VB y C) interfaz de Windows Media Player, se describe
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699557"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interfaz IWMPSettings (VB y C#)

Proporciona propiedades y métodos que obtienen o establecen los valores de configuración de Windows Media Player.

La interfaz **IWMPSettings** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPSettings (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPSettings (VB y C#)** tiene estos métodos.



| Método                                                               | Descripción                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Devuelve un valor que indica si el modo de bucle o el modo de orden aleatorio está activo.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.<br/>               |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPSettings (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                              | Tipo de acceso           | Descripción                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Automáticamente**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente. <br/>                                     |
| [**balancea**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el equilibrio estéreo actual.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en el contenido multimedia digital. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **comando** . <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor que indica si los cuadros de diálogo de error se muestran automáticamente.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador Web. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Solo lectura<br/>  | Obtiene un valor que indica si se puede realizar una acción especificada. En C#, este es el método **Get \_ isavailable** .<br/>             |
| [**silenciar**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece un valor que indica si el audio está silenciado. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece el número de veces que se reproducirá un elemento multimedia. <br/>                                                                         |
| [**Rate**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece la velocidad de reproducción actual del vídeo. <br/>                                                                                |
| [**cantidad**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lectura/escritura<br/> | Obtiene o establece el volumen de reproducción actual. <br/>                                                                                        |



 

Obtenga una interfaz **IWMPSettings** con la siguiente propiedad.



| Object                                                                   | Propiedad                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Configuración**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





