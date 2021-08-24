---
title: DRM_KeySeed
description: La propiedad KeySeed de DRM contiene el valor de ed. de clave que se usará junto con \_ keyID para crear la clave.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed windows Media Format
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46766dc5754bde33c00af250f03a54caf3c12c607ec14da858ac638a70f79baf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658976"
---
# <a name="drm_keyseed"></a>DRM \_ KeySeed

La **propiedad \_ KeySeed de DRM** contiene el valor de ed. de clave que se usará junto con keyID para crear la clave.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ KeySeed

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Esta propiedad se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). El objeto lector no puede acceder a él.

Normalmente, un valor de ed.clave se usa para proteger varios archivos o conjuntos de archivos, por ejemplo, todos los archivos emitidos por un servidor de licencias o quizás todos los archivos de un intérprete determinado. Sin embargo, KeyID es único para cada archivo.

El valor de ed. de clave debe seguir siendo un secreto que solo se comparte entre el creador del contenido y el distribuidor de licencias. Este valor no se almacena en el encabezado DRM y ni es necesario ni es accesible para las aplicaciones del reproductor DRM.

Se puede generar un nuevo valor de ed. de clave mediante el método [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) o cualquier otro medio adecuado.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




