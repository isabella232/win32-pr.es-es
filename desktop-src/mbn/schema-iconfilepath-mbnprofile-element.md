---
description: Contiene la ruta de acceso del archivo de icono de la conexión.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568672"
---
# <a name="iconfilepath-mbnprofile-element"></a>Elemento ICONFilePath (MBNProfile)

El **elemento ICONFilePath (MBNProfile)** contiene la ruta de acceso del archivo de icono de la conexión.

La interfaz de usuario de conexión del sistema operativo mostrará este icono cuando se realiza una conexión con este elemento.

Al pasar el XML para crear el perfil en el [**método CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) de la interfaz [**IMbnConnectionProfileManager,**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) esta ruta de acceso debe apuntar a la ubicación de origen del archivo de icono. Si se crea correctamente el objeto [**IMbnConnectionProfile,**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) el servicio Banda ancha móvil copiará el archivo de icono en su almacén interno y la ruta de acceso del perfil se modificará para reflejarlo.

El archivo de icono debe estar en .bmp con una dimensión de 32 x 32 píxeles.

Este elemento es una cadena de hasta 1024 caracteres, que contiene una ruta de acceso de archivo absoluta.

El elemento es opcional.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

El **elemento ICONFilePath** se define mediante el [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




