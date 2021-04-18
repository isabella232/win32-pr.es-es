---
description: Determina si una cadena Unicode coincide con el patrón especificado.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666175"
---
# <a name="rtlisnameinexpression-function"></a>RtlIsNameInExpression función)

Determina si una cadena Unicode coincide con el patrón especificado.

## <a name="syntax"></a>Sintaxis


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Expresión* \[ de de\]
</dt> <dd>

Puntero a la cadena de modelo. Esta cadena puede contener caracteres comodín. Si el parámetro *ignoreCase* es true, la cadena solo debe contener caracteres en mayúsculas.

</dd> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Puntero a la cadena que se va a comparar con el modelo. Esta cadena no puede contener caracteres comodín.

</dd> <dt>

*IgnoreCase* \[ de\]
</dt> <dd>

**True** para la coincidencia sin distinción entre mayúsculas y minúsculas, o **false** para la coincidencia con distinción de mayúsculas y minúsculas.

</dd> <dt>

*UpcaseTable* \[ en, opcional\]
</dt> <dd>

Un puntero opcional a una tabla de caracteres en mayúsculas que se va a utilizar para la coincidencia sin distinción entre mayúsculas y minúsculas. Si este parámetro es NULL, se utiliza la tabla de caracteres en mayúsculas predeterminada del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la cadena coincide con el patrón. Si la cadena no coincide con el patrón, esta función devuelve **false**.

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK) de Microsoft. También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                              |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
