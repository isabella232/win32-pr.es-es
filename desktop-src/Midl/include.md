---
title: include (atributo)
description: La instrucción include de ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- atributo include MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ec8deec34a42d39fc3973dff73e9912ecb96bfee62e348ef7aebfee6ee9f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067214"
---
# <a name="include-attribute"></a>include (atributo)

La instrucción **include de** ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombres* 
</dt> <dd>

Especifica el nombre de uno o varios archivos de encabezado del lenguaje C. Use el nombre de archivo completo, incluido . Extensión H y escriba cada nombre de archivo entre comillas. Separe varios nombres de archivo de encabezado de lenguaje C con comas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Como resultado de la instrucción **include,** el código auxiliar generado contendrá una instrucción include del preprocesador **\# C.** El archivo de encabezado del lenguaje C se proporciona al compilar los códigos auxiliares. Las instrucciones include se basan en el mecanismo del compilador de C para buscar archivos incluidos en la estructura de directorios.

> [!Note]  
> Use la [**directiva import**](import.md) en lugar de la directiva **include** para los archivos del sistema que contienen los tipos de datos que desea que estén disponibles para el archivo IDL. La **directiva import** omite los prototipos de función y permite usar modificadores del compilador MIDL que optimizan la generación de rutinas de soporte técnico.

 

## <a name="examples"></a>Ejemplos

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Importación**](import.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> </dl>

 

 




