---
description: El método MergeEx del objeto Merge es equivalente a la función Merge, salvo que toma un argumento adicional.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Método Merge.MergeEx (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071900"
---
# <a name="mergemergeex-method"></a>Método Merge.MergeEx

El **método MergeEx** del [**objeto Merge**](merge-object.md) es equivalente a la función [**Merge,**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) salvo que toma un argumento adicional. El *argumento pConfiguration* es una interfaz implementada por el cliente. El argumento puede ser NULL. La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.

El [**método Merge**](merge-merge.md) ejecuta una combinación de la base de datos actual y el módulo actual. La combinación asocia los componentes del módulo a la característica identificada por *la característica*. La raíz del árbol de directorios del módulo se redirige a la ubicación especificada por *RedirectDir*.

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

Nombre de una característica de la base de datos.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

Clave de una entrada en la tabla [Directory de](directory-table.md) la base de datos. Este parámetro puede ser null o una cadena vacía.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

El *argumento pConfiguration* es una interfaz implementada por el cliente. El argumento puede ser NULL. La presencia de este argumento indica que el cliente es capaz de admitir la funcionalidad de configuración, pero no obliga al cliente a proporcionar datos de configuración para ningún elemento configurable específico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una vez completada la combinación, los componentes del módulo se adjuntan a la característica identificada por *la característica*. Esta característica no se crea y debe ser una característica existente. El módulo se puede adjuntar a características adicionales mediante [**Conectar**](merge-connect.md) método .

Los cambios realizados en la base de datos se guardan si y solo si se llama al método [**CloseDatabase**](merge-closedatabase.md) con *bCommit* establecido en **TRUE.**

Si se produce algún conflicto de combinación, incluidas las exclusiones, se colocan en el enumerador de errores para su recuperación posterior, pero no hace que se produzca un error en la combinación. Los errores se pueden recuperar a través de [**la propiedad**](merge-errors.md) Errors. Los errores y los mensajes informativos se publican en el archivo de registro actual.

Cuando se produce un error en la combinación debido a una configuración incorrecta del módulo, la [**función MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) devuelve E \_ FAIL. Esto incluye estos errores msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType,** **msmErrorBadNullResponse,** **msmErrorMissingConfigItem** y **msmErrorDataRequestFailed**. Estos errores hacen que la combinación se detenga inmediatamente cuando se encuentra el error. El objeto de error se sigue agregando al enumerador cuando **MergeEx** devuelve E \_ FAIL. Para obtener más información sobre los errores de msmErrorType, [**vea get Type Function \_ (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Todos los demás errores hacen **que MergeEx** devuelva S \_ FALSE y haga que la combinación continúe.

### <a name="c"></a>C++

Vea [**Función MergeEx.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
