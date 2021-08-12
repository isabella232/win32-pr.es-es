---
title: Interfaz IWMPCdromRom (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos para administrar la creación de CD de audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Interfaz IWMPCdromRom (VB y C) Reproductor de Windows Media
- Interfaz IWMPCdromRom (VB y C) Reproductor de Windows Media , descrito
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
ms.openlocfilehash: 7731d5491e683c2a5d2e577c41dc96264c90f0d070538405d0fa3c3ea7283a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575963"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interfaz IWMPCdromRom (VB y C#)

Proporciona propiedades y métodos para administrar la creación de CD de audio.

## <a name="members"></a>Miembros

La **interfaz IWMPCdromRom (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPCdromRom (VB y C#)** tiene estos métodos.



| Método                                                                             | Descripción                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Borra el CD actual.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Recupera el valor del atributo especificado para el CD.<br/>    |
| [**Isavailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Proporciona información sobre la unidad de CD y los medios.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Actualiza la información de estado de la lista de reproducción de grabación actual.<br/> |
| [**start (Iniciar)/**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Desmantela el CD.<br/>                                                 |
| [**stop (Stop )Stop (Detener)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Detiene el proceso de grabación de CD.<br/>                                 |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPCdromRom (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                    | Tipo de acceso          | Descripción                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Solo lectura<br/> | Obtiene un valor que indica el tipo de CD que se va a grabar.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene la lista de reproducción actual que se va a grabar en el CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el progreso de la grabación de CD como porcentaje completado.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor de enumeración que indica el estado de la grabación actual.<br/> |
| [**Etiqueta**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Solo lectura<br/> | Obtiene la cadena de etiqueta del volumen de CD.<br/>                                 |



 

Obtenga una **interfaz IWMPCdromCombinación** mediante la conversión de la interfaz **IWMPCdrom** del CD que desea grabar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





