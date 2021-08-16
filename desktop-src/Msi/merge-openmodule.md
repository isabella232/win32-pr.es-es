---
description: El método OpenModule del objeto Merge abre un módulo de Windows installer en modo de solo lectura. Se debe abrir un módulo para poder combinarlo con una base de datos de instalación.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Método Merge.OpenModule (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4659fbd2c96d883b04e653fc67c6aa3017f16135405f956bf9b4eb78101bb404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628731"
---
# <a name="mergeopenmodule-method"></a>Método Merge.OpenModule

El **método OpenModule** del objeto [**Merge**](merge-object.md) abre un módulo de combinación Windows Installer en modo de solo lectura. Se debe abrir un módulo para poder combinarlo con una base de datos de instalación.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nombre de archivo completo que apunta a un módulo de combinación.

</dd> <dt>

*Lenguaje* 
</dt> <dd>

Identificador de idioma válido (LANGID).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función abre el módulo merge en modo de solo lectura y excluye que otros programas escriban en el módulo merge hasta que se llame [**al método CloseModule.**](merge-closemodule.md)

El instalador intenta abrir el módulo en el idioma especificado por *Idioma* o en un idioma más general. Por ejemplo, si *Language* se especifica como 1033, se puede abrir un módulo con un idioma predeterminado de 1033, 9 o 0 en su idioma predeterminado. Un *valor* de Idioma de 9 abre los módulos con un idioma predeterminado de 9 o 0. Si el idioma predeterminado del módulo no cumple los requisitos especificados, se intenta transformar el módulo al idioma solicitado. Si se produce un error, el módulo se transforma en idiomas cada vez más generales, hasta que el idioma es neutro. Si ninguna de las transformaciones se realiza correctamente, el módulo no se puede abrir. En este caso, se agrega un error a la lista de errores de tipo msmErrorLanguageUnsupported. Si se produce un error al transformar el módulo al idioma deseado, se agrega un error a la lista de errores de tipo msmErrorLanguageFailed. Para obtener más información, [**vea la propiedad Type**](error-type.md) del objeto [**Error.**](error-object.md) Al abrir un módulo de combinación se borran los errores que aún no se han recuperado.

### <a name="c"></a>C++

Consulte [**Función OpenModule.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
