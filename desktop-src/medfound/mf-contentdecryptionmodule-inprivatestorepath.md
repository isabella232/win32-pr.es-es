---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244778"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>Propiedad \_ INPRIVATESTOREPATH DE MF CONTENTDECRYPTIONMODULE \_

Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.


## <a name="data-type"></a>Tipo de datos

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Valor de propiedad

Ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.

## <a name="remarks"></a>Comentarios

La aplicación debe eliminar la ubicación de la tienda después de que se haya publicado el objeto de CDM.

Si no se establece esta propiedad, el sistema usará la ruta de acceso especificada con la [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) para los datos específicos del contenido.

Establezca esta propiedad al crear un CDM mediante una llamada a [CRYPTOContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 Actualización de abril de 2020<br/>                                     |
| Header<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

- [Media Foundation propiedades](media-foundation-properties.md)
- [CRYPTOContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




