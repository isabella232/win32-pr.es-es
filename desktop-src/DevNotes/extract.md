---
description: La función Extract extrae los archivos de un archivo. cab.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extraer función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649949"
---
# <a name="extract-function"></a>Extraer función

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]

La función **Extract** extrae los archivos de un archivo. cab.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PS* 
</dt> <dd>

Puntero a una estructura de [**sesión**](session.md) que contiene información sobre la sesión actual.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Puntero al nombre del archivo. cab del que se van a extraer los archivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Fun**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**SESIÓN**](session.md)
</dt> </dl>

 

 
