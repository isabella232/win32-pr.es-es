---
title: Media. error
description: La propiedad error recupera un objeto ErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Medio. error de Windows Media Player
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
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653503"
---
# <a name="mediaerror"></a>Media. error

La propiedad **error** recupera un objeto **ErrorItem** si el elemento multimedia tiene una condición de error.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. **error** de

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **ErrorItem** de solo lectura.

## <a name="remarks"></a>Observaciones

Si no se puede reproducir el elemento multimedia, esta propiedad recupera un objeto **ErrorItem** que contiene información sobre el problema encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





