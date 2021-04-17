---
description: El método OpenModule del objeto Merge abre un módulo de combinación de Windows Installer en modo de solo lectura. Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule (método) (Mergemod. h)
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
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681305"
---
# <a name="mergeopenmodule-method"></a>Merge. OpenModule (método)

El método **OpenModule** del objeto [**Merge**](merge-object.md) abre un módulo de combinación de Windows Installer en modo de solo lectura. Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.

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

Identificador de idioma (LANGID) válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función abre el módulo de combinación en modo de solo lectura y evita que otros programas escriban en el módulo de combinación hasta que se llama al método [**CloseModule**](merge-closemodule.md) .

El instalador intenta abrir el módulo en el idioma especificado por *Language* o en un lenguaje más general. Por ejemplo, si *Language* se especifica como 1033, se puede abrir un módulo con un idioma predeterminado de 1033, 9 o 0 en su idioma predeterminado. Un valor de *idioma* de 9 abre los módulos con un idioma predeterminado de 9 o 0. Si el idioma predeterminado del módulo no cumple los requisitos especificados, se realiza un intento de transformar el módulo en el idioma solicitado. Si se produce un error, el módulo se transforma en lenguajes cada vez más generales, hasta el lenguaje neutro. Si ninguna de las transformaciones se realiza correctamente, el módulo no se abre. En este caso, se agrega un error a la lista de errores de tipo msmErrorLanguageUnsupported. Si se produce un error al transformar el módulo en el idioma deseado, se agrega un error a la lista de errores de tipo msmErrorLanguageFailed. Para obtener más información, vea la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) . Al abrir un módulo de combinación, se borran los errores que aún no se han recuperado.

### <a name="c"></a>C++

Consulte función [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
