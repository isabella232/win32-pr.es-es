---
description: Convierte una estructura DEVMODE en un vale de impresión.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: Función ConvertDevModeToPrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268372"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>Función ConvertDevModeToPrintTicketThunk2

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTConvertDevModeToPrintTicket proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) una funcionalidad equivalente y se debe usar en su lugar.\]

Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un vale de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ En\]
</dt> <dd>

Identificador de un proveedor de vales de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pDevmode* \[ En\]
</dt> <dd>

Puntero al [**DEVMODE que**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se convertirá.

</dd> <dt>

*cbSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado *en pDevmode*.

</dd> <dt>

*ámbito* \[ En\]
</dt> <dd>

Valor que especifica el ámbito de *ppPrintTicket.* Este valor puede especificar una sola página, un documento completo o todos los documentos del trabajo de impresión. El valor de este parámetro debe ser miembro de la enumeración [**EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) que se convierte como **DWORD.**

</dd> <dt>

*ppPrintTicket* \[ out\]
</dt> <dd>

Dirección del búfer que contiene un vale de impresión que representa el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado *en pDevmode*. Esta función llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar este búfer. Cuando el búfer ya no es necesario, el autor de la llamada debe liberarlo mediante una [**llamada a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*printPrintTicketLength* \[ out\]
</dt> <dd>

Tamaño, en bytes, del vale de impresión devuelto en *ppPrintTicket.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error **HRESULT.** Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

