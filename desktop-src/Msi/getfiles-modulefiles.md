---
description: La propiedad ModuleFiles del objeto GetFiles devuelve todas las claves principales de la tabla de archivos para el módulo actualmente abierto.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Propiedad GetFiles. ModuleFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671651"
---
# <a name="getfilesmodulefiles-property"></a>Propiedad GetFiles. ModuleFiles

La propiedad **ModuleFiles** del objeto [**GetFiles**](getfiles-object.md) devuelve todas las claves principales de la [tabla de archivos](file-table.md) para el módulo actualmente abierto. Las claves principales se devuelven como una colección de cadenas. El módulo debe abrirse mediante una llamada al método [**OpenModule**](merge-openmodule.md) del [objeto Merge](merge-object.md) antes de llamar a **ModuleFiles**.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Tenga en cuenta que el orden de los archivos enumerados en la colección puede no estar en la misma secuencia que se muestra en la tabla de archivos.

Si el módulo no tiene ninguna tabla de archivos o no contiene ningún archivo en el idioma en particular, ModuleFiles devuelve una colección vacía de cadenas.

### <a name="c"></a>C++

Consulte [**Get \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
