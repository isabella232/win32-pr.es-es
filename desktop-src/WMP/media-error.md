---
title: Media.error
description: La propiedad error recupera un objeto ErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media.error Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967500"
---
# <a name="mediaerror"></a>Media.error

La **propiedad error** recupera un objeto **ErrorItem** si el elemento multimedia tiene una condición de error.

## <a name="syntax"></a>Sintaxis

*player*. *currentMedia*. **error**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **ErrorItem de solo** lectura.

## <a name="remarks"></a>Observaciones

Si no se puede reproducir el elemento multimedia, esta propiedad recupera un **objeto ErrorItem** que contiene información sobre el problema detectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





