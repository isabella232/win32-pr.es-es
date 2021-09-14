---
description: Completa las operaciones necesarias en el búfer de metadatos y libera el objeto ISpatialAudioMetadataItems especificado.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: ISpatialAudioMetadataWriter::Close (Método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164962"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>ISpatialAudioMetadataWriter::Close (Método)

Completa las operaciones necesarias en el búfer de metadatos y libera el objeto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, los posibles códigos de retorno incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                     | Descripción                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ NO \_ ITEMS \_ OPEN**</dt> </dl>            | [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) proporcionado no se ha abierto con una llamada a [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ NO \_ ITEMS \_ WRITTEN**</dt> </dl>         | No se ha escrito ningún elemento de metadatos en el [**objeto ISpatialAudioMetadataItems proporcionado.**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)<br/>                                              |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT E ITEM DEBE \_ TENER \_ \_ \_ \_ COMANDOS**</dt> </dl> | No se ha escrito ningún comando de metadatos en el [**objeto ISpatialAudioMetadataItems proporcionado.**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)<br/>                                           |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




