---
description: Guarda los cambios en un perfil en el disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile:: Save (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542806"
---
# <a name="iscanprofilesave-method"></a>IScanProfile:: Save (método)

Guarda los cambios en un perfil en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Un perfil de digitalización guardado es un archivo XML almacenado en% USERPROFILE% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.

Si más de un proceso escribe en el objeto [**IScanProfile**](-wia-iscanprofile.md) , el que llama a **IScanProfile:: Save** Last es el único proceso cuyos cambios se guardan.

El método **IScanProfile:: Save** valida el perfil antes de guardarlo. El perfil siempre se considera válido a menos que la categoría del elemento 2,0 de adquisición de imágenes de Windows (WIA) asociada al perfil sea el alimentador de la categoría WIA \_ \_ o el \_ alimentador de la categoría WIA \_ . Si la categoría es la \_ categoría \_ de WIA plana o el \_ \_ alimentador de la categoría WIA, las siguientes propiedades deben ser válidas para el elemento, si las propiedades están contenidas en el perfil:

\_brillo de IP de WIA \_

\_contraste de IP de WIA \_

tipo de DataType del \_ IPA de WIA \_

\_XRES de IP WIA \_

\_formato de IPA de WIA \_

Además, si la categoría es \_ alimentador de categoría WIA \_ , la \_ propiedad tamaño de página de IPS de WIA \_ \_ debe ser válida, si está presente en el perfil. Para obtener más información sobre estas propiedades, consulte el artículo sobre las constantes de las propiedades de los [**elementos de WIA**](-wia-wiaitempropscanneritem.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




