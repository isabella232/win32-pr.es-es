---
title: DRM_KeyID
description: El atributo KeyID de DRM \_ contiene el identificador de clave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID windows Media Format
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c274123c04272fa4ba684a00f5d8f58fc395ce25e8b38bab534007d878c350e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027873"
---
# <a name="drm_keyid"></a>DRM \_ KeyID

El **atributo \_ KeyID de DRM** contiene el identificador de clave.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ KeyID

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente para el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). El mismo atributo de archivo se puede recuperar mediante [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md).

El identificador de clave se usa junto con el valor de ed. de clave para crear la clave de contenido que se usa para cifrar y descifrar el archivo. La aplicación de escritura usa el identificador de clave para cifrar el archivo y, a continuación, almacena el identificador de clave en el encabezado de archivo. Cuando una aplicación de reproductor solicita una licencia para un archivo, el componente DRM envía el identificador de clave (junto con el resto del encabezado DRM) al servidor de licencias. El servidor de licencias, que tiene la ed. de clave secreta, la usa y el identificador de clave para crear una clave para el archivo, que luego inserta en una licencia junto con los distintos derechos que se aplicarán al archivo.

Normalmente, se usa un valor de ed. de clave con muchos iDs de clave. El valor de ed.clave es un secreto compartido solo por el creador del contenido y el distribuidor de licencias. El identificador de clave lo usan las aplicaciones cliente DRM y se almacena en el encabezado DRM sin cifrado.

Este atributo es el mismo que [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




