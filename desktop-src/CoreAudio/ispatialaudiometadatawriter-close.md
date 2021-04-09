---
description: Completa cualquier operación necesaria en el búfer de metadatos y libera el objeto ISpatialAudioMetadataItems especificado.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'ISpatialAudioMetadataWriter:: Close (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153343"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>ISpatialAudioMetadataWriter:: Close (método)

Completa cualquier operación necesaria en el búfer de metadatos y libera el objeto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, los códigos de retorno posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                     | Descripción                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ no hay ningún \_ elemento \_ abierto**</dt> </dl>            | El [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) proporcionado no se ha abierto con una llamada a [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ no hay \_ elementos \_ escritos**</dt> </dl>         | No se ha escrito ningún elemento de metadatos en el [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)proporcionado.<br/>                                              |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ Item \_ deben \_ tener \_ comandos**</dt> </dl> | No se han escrito comandos de metadatos en el [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)proporcionado.<br/>                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




