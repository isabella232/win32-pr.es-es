---
title: MetadataPicture.description
description: La propiedad description recupera una descripción de la imagen de metadatos.
ms.assetid: 7a07a8a0-d50a-4951-95a8-c1285a1be737
keywords:
- MetadataPicture.description Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture.description
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbacd8f2fbded3501100809de166651ca56cca8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361728"
---
# <a name="metadatapicturedescription"></a>MetadataPicture.description

La **propiedad description** recupera una descripción de la imagen de metadatos.

## <a name="syntax"></a>Sintaxis

*player*. *currentMedia*. **getItemInfoByType**( *name*, *language*, *index*). **descripción**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MetadataPicture (objeto)**](metadatapicture-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





