---
title: include (atributo)
description: La instrucción de inclusión ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- atributo de inclusión MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148889"
---
# <a name="include-attribute"></a>include (atributo)

La instrucción de **inclusión** ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombres* 
</dt> <dd>

Especifica el nombre de uno o más archivos de encabezado de lenguaje C. Use el nombre de archivo completo, incluido. H y escriba cada nombre de archivo entre comillas. Separe varios nombres de archivo de encabezado de lenguaje C con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Como resultado de la instrucción **include** , el código auxiliar generado contendrá una instrucción **\# include** de C-preprocesador. El archivo de encabezado del lenguaje C se proporciona al compilar el código auxiliar. Las instrucciones include se basan en el mecanismo del compilador de C para buscar archivos incluidos en la estructura de directorios.

> [!Note]  
> Use la Directiva de [**importación**](import.md) en lugar de la directiva **include** para los archivos del sistema que contengan tipos de datos que desee poner a disposición del archivo IDL. La Directiva de **importación** omite los prototipos de función y permite utilizar modificadores de compilador MIDL que optimizan la generación de rutinas de soporte.

 

## <a name="examples"></a>Ejemplos

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**importar**](import.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> </dl>

 

 




