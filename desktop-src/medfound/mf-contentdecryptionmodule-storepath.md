---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497668"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>\_ \_ Propiedad STOREPATH de MF CONTENTDECRYPTIONMODULE

Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.


## <a name="data-type"></a>Tipo de datos

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valor de propiedad

Una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.

## <a name="remarks"></a>Observaciones

La ruta de acceso especificada con esta propiedad también se utilizará para los datos específicos del contenido si no se ha establecido la propiedad [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) .

Para mejorar el rendimiento de COM, la aplicación no debe eliminar la ubicación del almacén una vez liberado el objeto CDM.



Establezca esta propiedad al crear un CDM llamando a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Actualización 2020 de abril de Windows 10<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vea también

- [Propiedades de Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




