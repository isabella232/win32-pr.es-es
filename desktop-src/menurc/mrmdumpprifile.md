---
title: Función MrmDumpPriFile (MrmResourceIndexer. h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco), con el fin de que sea más fácil de leer.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menús de la función MrmDumpPriFile y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802521"
---
# <a name="mrmdumpprifile-function"></a>MrmDumpPriFile función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco), con el fin de que sea más fácil de leer. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexFileName* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso completa a un archivo PRI. Este es el archivo PRI que se volcará en XML.

</dd> <dt>

*schemaPriFile* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso de archivo completa opcional a un archivo de esquema (o a un archivo PRI que representa un esquema; vea la sección comentarios).

</dd> <dt>

*dumpType* \[ de\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Especifica el grado de detalle del volcado XML o de si se debe volcar un esquema.

</dd> <dt>

*outputXmlFile* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso de un archivo XML que se va a crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el modificador *OMITSCHEMAFROMRESOURCEPACKS* en el archivo de configuración de PRI). Para volcar un paquete de recursos sin esquemas, pase la ruta de acceso a los datos del paquete principal de PRI como argumento para el parámetro *schemaPriFile* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

