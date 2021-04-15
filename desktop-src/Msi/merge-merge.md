---
description: El método Merge del objeto Merge ejecuta una combinación de la base de datos actual y el módulo actual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge (método) (Mergemod. h)
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
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653903"
---
# <a name="mergemerge-method"></a>Merge. Merge (método)

El método **Merge** del objeto [**Merge**](merge-object.md) ejecuta una combinación de la base de datos actual y el módulo actual. La combinación adjunta los componentes del módulo a la característica identificada por la *característica*. La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.

Solo se puede llamar una vez al método **Merge** para combinar una combinación determinada de archivos. msi y. msm.

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

El nombre de una característica en la base de datos.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

La clave de una entrada en la [tabla de directorios](directory-table.md) de la base de datos. Este parámetro puede ser null o una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por la *característica*. Esta característica no se crea y debe ser una característica existente. Tenga en cuenta que el método **Merge** obtiene todas las referencias de características en el módulo y sustituye la referencia de características de todas las apariciones del GUID null en la base de datos del módulo. Para obtener más información, vea [hacer referencia a características en módulos de combinación](referencing-features-in-merge-modules.md).

El módulo se puede adjuntar a características adicionales mediante el método [**Connect**](merge-connect.md) . Tenga en cuenta que llamar al método **Connect** solo crea asociaciones de componentes de características. No modifica las filas que ya se han combinado en la base de datos.

Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CerrarBaseDeDatos**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) con *BCommit* establecido en **true**.

Si se producen conflictos de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su posterior recuperación, pero no se produce un error en la combinación. Los errores se pueden recuperar a través de la propiedad [**errores**](error-object.md) . Los errores y los mensajes informativos se publican en el archivo de registro actual.

### <a name="c"></a>C++

Vea función [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
