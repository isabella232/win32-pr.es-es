---
description: El método Merge del objeto Merge ejecuta una combinación de la base de datos actual y el módulo actual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Método Merge.Merge (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804735"
---
# <a name="mergemerge-method"></a>Método Merge.Merge

El **método Merge** del objeto [**Merge**](merge-object.md) ejecuta una combinación de la base de datos actual y el módulo actual. La combinación asocia los componentes del módulo a la característica identificada por *la característica*. La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.

Solo **se** puede llamar al método Merge una vez para combinar una combinación determinada de archivos .msi y .msm.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Característica* 
</dt> <dd>

Nombre de una característica de la base de datos.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

Clave de una entrada en la tabla [Directory de](directory-table.md) la base de datos. Este parámetro puede ser null o una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por *la característica*. Esta característica no se crea y debe ser una característica existente. Tenga en cuenta que el **método Merge** obtiene todas las referencias de características del módulo y sustituye la referencia de características por todas las apariciones del GUID nulo en la base de datos del módulo. Para obtener más información, vea [Hacer referencia a características en módulos de mezcla.](referencing-features-in-merge-modules.md)

El módulo se puede adjuntar a características adicionales mediante [**el Conectar**](merge-connect.md) método . Tenga en cuenta que al **llamar al Conectar** de características solo se crean asociaciones de componentes de características. No modifica las filas que ya se han combinado en la base de datos.

Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) con *bCommit* establecido en **TRUE.**

Si se produce algún conflicto de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su recuperación posterior, pero no hace que se produzca un error en la combinación. Los errores se pueden recuperar a través de [**la propiedad Errors.**](error-object.md) Los errores y los mensajes informativos se publican en el archivo de registro actual.

### <a name="c"></a>C++

Vea [**Función Merge.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
