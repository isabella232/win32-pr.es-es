---
title: Interfaz IWMPCdromBurn (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para administrar la creación de CDs de audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- IWMPCdromBurn (VB y C) interfaz de Windows Media Player
- IWMPCdromBurn (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690692"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interfaz IWMPCdromBurn (VB y C#)

Proporciona propiedades y métodos para administrar la creación de CDs de audio.

## <a name="members"></a>Miembros

La interfaz **IWMPCdromBurn (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPCdromBurn (VB y C#)** tiene estos métodos.



| Método                                                                             | Descripción                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Borra el CD actual.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Recupera el valor del atributo especificado para el CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Proporciona información acerca de la unidad de CD y el medio.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Actualiza la información de estado de la lista de reproducción de grabación actual.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Graba el CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Detiene el proceso de grabación de CD.<br/>                                 |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPCdromBurn (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                    | Tipo de acceso          | Descripción                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Solo lectura<br/> | Obtiene un valor que indica el tipo de CD que se va a grabar.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene la lista de reproducción actual que se va a grabar en el CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el progreso de la grabación del CD como porcentaje completado.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor de enumeración que indica el estado actual de la grabación.<br/> |
| [**rótulo**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Solo lectura<br/> | Obtiene la cadena de etiqueta del volumen del CD.<br/>                                 |



 

Obtenga una interfaz **IWMPCdromBurn** mediante la conversión de la interfaz **IWMPCdrom** del CD que desea grabar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





