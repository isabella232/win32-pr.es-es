---
title: Función MrmDumpPriDataInMemory (MrmResourceIndexer. h)
description: Vuelca la información de PRI (como un BLOB en memoria, creada por una llamada anterior a MrmCreateResourceFileInMemory) a su equivalente XML (como datos en memoria), para que sea más fácil de leer.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menús de la función MrmDumpPriDataInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666054"
---
# <a name="mrmdumppridatainmemory-function"></a>MrmDumpPriDataInMemory función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Vuelca la información de PRI (como un BLOB en memoria, creada por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) a su equivalente XML (como datos en memoria), para que sea más fácil de leer. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData*. Llame a [**MrmFreeMemory**](mrmfreememory.md) con el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inputPriData* \[ de\]
</dt> <dd>

Tipo: **byte \** _

Un puntero a los datos de PRI creados por una llamada anterior a [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md).

</dd> <dt>

*inputPriSize* \[ de\]
</dt> <dd>

Tipo: **ULong**

Tamaño de los datos a los que apunta *inputPriData*.

</dd> <dt>

*schemaPriData* \[ en, opcional\]
</dt> <dd>

Tipo: **byte \** _

Un puntero opcional a la información de PRI (como un BLOB en memoria) que representa los datos de esquema creados por una llamada anterior a [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md). No libere *schemaPriData* hasta que termine de usar el indizador de recursos. Vea también la sección Comentarios.

</dd> <dt>

*schemaPriSize* \[ de\]
</dt> <dd>

Tipo: **ULong**

Tamaño de los datos a los que apunta *schemaPriData*.

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

Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el modificador *OMITSCHEMAFROMRESOURCEPACKS* en el archivo de configuración de PRI). Para volcar un paquete de recursos sin esquemas, pase la ruta de acceso a los datos del paquete principal de PRI como argumento para el parámetro *schemaPriData* .

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

 

