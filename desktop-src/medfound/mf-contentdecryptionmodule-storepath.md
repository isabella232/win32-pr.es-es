---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579913"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH, propiedad

Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.


## <a name="data-type"></a>Tipo de datos

**LPWSTR** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>Valor de propiedad

Ruta de acceso de archivo que representa una ubicación de almacenamiento que el Módulo de descifrado de contenido (CDM) puede usar para la inicialización.

## <a name="remarks"></a>Observaciones

La ruta de acceso especificada con esta propiedad también se usará para los datos específicos del contenido [si no MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) propiedad predeterminada.

Para mejorar el rendimiento com, la aplicación no debe eliminar la ubicación del almacén después de que se haya publicado el objeto de CDM.



Establezca esta propiedad al crear un CDM mediante una llamada a [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 Actualización de abril de 2020<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vea también

- [Media Foundation propiedades](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




