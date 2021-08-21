---
title: Media.error
description: La propiedad error recupera un objeto ErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Archivo Media.error Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 709e6318e125d515eb06d86147cb71f6a2601caf526b43416e5493c8aaef044d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837178"
---
# <a name="mediaerror"></a>Media.error

La **propiedad error** recupera un objeto **ErrorItem** si el elemento multimedia tiene una condición de error.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **error**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **ErrorItem de solo** lectura.

## <a name="remarks"></a>Comentarios

Si no se puede reproducir el elemento multimedia, esta propiedad recupera un **objeto ErrorItem** que contiene información sobre el problema detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





