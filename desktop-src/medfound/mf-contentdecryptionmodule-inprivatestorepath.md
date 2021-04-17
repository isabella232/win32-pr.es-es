---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542558"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>\_ \_ Propiedad INPRIVATESTOREPATH de MF CONTENTDECRYPTIONMODULE

Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.


## <a name="data-type"></a>Tipo de datos

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**

## <a name="property-value"></a>Valor de propiedad

Una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.

## <a name="remarks"></a>Observaciones

La aplicación debe eliminar la ubicación del almacén una vez liberado el objeto CDM.

Si no se establece esta propiedad, el sistema usará la ruta de acceso especificada con la propiedad [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) para los datos específicos del contenido.

Establezca esta propiedad al crear un CDM llamando a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Actualización 2020 de abril de Windows 10<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vea también

- [Propiedades de Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




