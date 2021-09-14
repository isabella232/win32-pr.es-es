---
description: La propiedad ModuleFiles del objeto GetFiles devuelve todas las claves principales de la tabla File para el módulo abierto actualmente.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Propiedad GetFiles.ModuleFiles (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074732"
---
# <a name="getfilesmodulefiles-property"></a>GetFiles.ModuleFiles, propiedad

**La propiedad ModuleFiles** del [**objeto GetFiles**](getfiles-object.md) devuelve todas las claves principales de la [tabla File](file-table.md) para el módulo abierto actualmente. Las claves principales se devuelven como una colección de cadenas. El módulo debe abrirse mediante una llamada al método [**OpenModule**](merge-openmodule.md) del objeto [Merge antes](merge-object.md) de llamar a **ModuleFiles.**

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Tenga en cuenta que es posible que el orden de los archivos enumerados en la colección no esté en la misma secuencia que en la tabla Archivo.

Si el módulo no tiene ninguna tabla File o no contiene archivos en el lenguaje determinado, ModuleFiles devuelve una colección vacía de cadenas.

### <a name="c"></a>C++

Consulte [**la función get \_ ModuleFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
