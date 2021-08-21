---
description: La función Extract extrae archivos de un archivador.
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
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162069"
---
# <a name="extract-function"></a>Extraer función

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]

La **función Extract** extrae archivos de un archivador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ps* 
</dt> <dd>

Puntero a una [**estructura SESSION**](session.md) que contiene información sobre la sesión actual.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Puntero al nombre del gabinete del que se van a extraer los archivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Erf**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

 
