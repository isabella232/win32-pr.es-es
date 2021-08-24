---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8126bfea15f9946bb9950293a6c39c101f9c37c8870176fb4bb0108aa5862bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723465"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>Propiedad \_ MF CONTENTDECRYPTIONMODULE \_ STOREPATH

Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.


## <a name="data-type"></a>Tipo de datos

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valor de propiedad

Ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.

## <a name="remarks"></a>Comentarios

La ruta de acceso especificada con esta propiedad también se usará para los datos específicos del contenido si no [se MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) la propiedad .

Para mejorar el rendimiento COM, la aplicación no debe eliminar la ubicación del almacén después de que se haya publicado el objeto de CDM.



Establezca esta propiedad al crear un CDM mediante una llamada a [CRYPTOContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 Actualización de abril de 2020<br/>                                     |
| Header<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vea también

- [Media Foundation propiedades](media-foundation-properties.md)
- [CRYPTOContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




