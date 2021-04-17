---
description: El método MergeEx del objeto Merge es equivalente a la función Merge, salvo que toma un argumento adicional.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Método Merge. MergeEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679283"
---
# <a name="mergemergeex-method"></a>Merge. MergeEx (método)

El método **MergeEx** del objeto [**Merge**](merge-object.md) es equivalente a la función [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , salvo que toma un argumento adicional. El argumento *pConfiguration* es una interfaz implementada por el cliente. El argumento puede ser null. La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.

El método [**Merge**](merge-merge.md) ejecuta una combinación de la base de datos actual y el módulo actual. La combinación adjunta los componentes del módulo a la característica identificada por la *característica*. La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
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

</dd> <dt>

*pConfiguration* 
</dt> <dd>

El argumento *pConfiguration* es una interfaz implementada por el cliente. El argumento puede ser null. La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por la *característica*. Esta característica no se crea y debe ser una característica existente. El módulo se puede adjuntar a características adicionales mediante el método [**Connect**](merge-connect.md) .

Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CerrarBaseDeDatos**](merge-closedatabase.md) con *BCommit* establecido en **true**.

Si se producen conflictos de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su posterior recuperación, pero no se produce un error en la combinación. Los errores se pueden recuperar a través de la propiedad [**errores**](merge-errors.md) . Los errores y los mensajes informativos se publican en el archivo de registro actual.

Cuando se produce un error en la combinación debido a una configuración incorrecta del módulo, la función [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) devuelve E \_ Fail. Esto incluye estos errores de msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** y **msmErrorDataRequestFailed**. Estos errores hacen que la combinación se detenga inmediatamente cuando se produce el error. El objeto de error se sigue agregando al enumerador cuando **MergeEx** devuelve E \_ Fail. Para obtener más información sobre los errores de msmErrorType, consulte [**Get \_ Type function (objeto de error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Todos los demás errores hacen que **MergeEx** devuelva S \_ false y provoque que la combinación continúe.

### <a name="c"></a>C++

Consulte función [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
