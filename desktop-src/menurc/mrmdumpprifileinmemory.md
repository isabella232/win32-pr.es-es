---
title: Función MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria), para que sea más fácil de leer.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menús de la función MrmDumpPriFileInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665922"
---
# <a name="mrmdumpprifileinmemory-function"></a>MrmDumpPriFileInMemory función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria), para que sea más fácil de leer. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*. Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
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

*outputXmlData* \[ enuncia\]
</dt> <dd>

Tipo: **byte \* \***

Dirección de un puntero a BYTE. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*. Llame a [**MrmFreeMemory**](mrmfreememory.md) con el puntero en byte para liberar esa memoria.

</dd> <dt>

*outputXmlSize* \[ enuncia\]
</dt> <dd>

Tipo: **ULong \** _

Dirección de un ULONG. En _outputXmlSize *, la función devuelve el tamaño de la memoria asignada a la que apunta *outputXmlData*.

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

 

