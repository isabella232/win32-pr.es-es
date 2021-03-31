---
description: Establece una confianza de código dinámico de CRL de .NET en disco para .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Función WldpSetDynamicCodeTrust (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423291"
---
# <a name="wldpsetdynamiccodetrust-function"></a>WldpSetDynamicCodeTrust función)

Establece una confianza de código dinámico de CRL de .NET en disco para .NET.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileHandle* 
</dt> <dd>

Identificador de un archivo de código dinámico en disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




