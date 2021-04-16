---
description: Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649673"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace función)

Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo **sprintf**.

## <a name="syntax"></a>Sintaxis


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Parámetro de seguimiento de 32 bits que se usa para el filtrado en el nivel de la aplicación.

</dd> <dt>

*szFormat* 
</dt> <dd>

Cadena terminada en cero que describe el formato del seguimiento.

</dd> <dt>

*dor* 
</dt> <dd>

Un marcador para las funciones de **vsprintf** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve la longitud de la instrucción de seguimiento, en bytes.

## <a name="remarks"></a>Observaciones

Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el protocolo de transferencia de noticias en red (NNTP).

El tipo de datos de la **\_ lista va** es un tipo estándar que se usa para almacenar la información necesaria para las macros de fin **\_ arg** y **\_ fin** . Para obtener más información, consulte [tipos estándar](/cpp/c-runtime-library/standard-types?view=vs-2019).

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

