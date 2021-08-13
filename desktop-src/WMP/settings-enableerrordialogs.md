---
title: Configuración.enableErrorDialogs
description: La propiedad enableErrorDialogs especifica o recupera un valor que indica si los cuadros de diálogo de error se muestran automáticamente.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Configuración.enableErrorDialogs Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa786606a97edcfca22512dd0b3188a06a7851f8bab2401e139d7ead2c3495ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569377"
---
# <a name="settingsenableerrordialogs"></a>Configuración.enableErrorDialogs

La **propiedad enableErrorDialogs** especifica o recupera un valor que indica si los cuadros de diálogo de error se muestran automáticamente.

## <a name="syntax"></a>Syntax

player.settings.enableErrorDialogs

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Valor | Descripción                                     |
|-------|-------------------------------------------------|
| true  | Predeterminada. Los cuadros de diálogo de error se muestran automáticamente. |
| false | Los cuadros de diálogo de error no se muestran automáticamente.      |



 

## <a name="remarks"></a>Comentarios

Esta propiedad muestra un comportamiento específico para las instancias remotas del control Player. Para obtener más información, [vea Remoting the Reproductor de Windows Media Control](remoting-the-windows-media-player-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





