---
title: DRM_KeySeed
description: La \_ propiedad KeySeed de DRM contiene la inicialización de clave que se utilizará junto con el ID. de clave para crear la clave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676345"
---
# <a name="drm_keyseed"></a>\_KEYSEED DRM

La **propiedad \_ KeySeed de DRM** contiene la inicialización de clave que se utilizará junto con el ID. de clave para crear la clave.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ KeySeed

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Esta propiedad se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). No es accesible para el objeto lector.

Una inicialización de clave se usa normalmente para proteger varios archivos o conjuntos de archivos, por ejemplo, todos los archivos emitidos por un servidor de licencias, o quizás todos los archivos de un intérprete determinado. Sin embargo, el ID. de la archivo es único para cada archivo.

La inicialización de clave debe ser un secreto que solo se comparta entre el creador de contenido y el distribuidor de licencias. Este valor no se almacena en el encabezado DRM y no es necesario ni está accesible para las aplicaciones de reproductor DRM.

Se puede generar un nuevo inicialización de clave mediante el método [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o cualquier otro medio adecuado.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




