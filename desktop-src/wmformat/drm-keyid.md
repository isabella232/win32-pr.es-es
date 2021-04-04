---
title: DRM_KeyID
description: El atributo id. de clave de DRM \_ contiene el identificador de clave.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077348"
---
# <a name="drm_keyid"></a>ID. de ID \_ de DRM

El atributo id. de clave de **DRM \_** contiene el identificador de clave.

## <a name="global-constant"></a>Constante global

ID. de \_ wszWMDRM g \_

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente para el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Se puede recuperar el mismo atributo de archivo mediante el ID. de [**\_ \_ DRMHeader de DRM**](drm-drmheader-keyid.md).

El identificador de clave se utiliza junto con la inicialización de clave para crear la clave de contenido que se usa para cifrar y descifrar el archivo. La aplicación de escritura usa el identificador de clave para cifrar el archivo y, a continuación, almacena el identificador de clave en el encabezado del archivo. Cuando una aplicación de reproducción solicita una licencia para un archivo, el componente DRM envía el identificador de clave (junto con el resto del encabezado DRM) al servidor de licencias. El servidor de licencias, que tiene la clave secreta SEED, lo utiliza y el identificador de clave para crear una clave para el archivo, que después inserta en una licencia junto con los distintos derechos que se aplicarán al archivo.

Normalmente, se usa una inicialización de clave con varios identificadores de clave. La inicialización de clave es un secreto compartido solo por el creador de contenido y el distribuidor de licencias. El identificador de clave lo usan las aplicaciones cliente de DRM y se almacena en el encabezado DRM en el borrado.

Este atributo es igual que el ID. de [**\_ \_ DRMHeader de DRM**](drm-drmheader-keyid.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




