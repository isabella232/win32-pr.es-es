---
description: Convierte una estructura DEVMODE en una solicitud de impresión.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677725"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2 función)

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]

Convierte una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en una solicitud de impresión.

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

*hProvider* \[ de\]
</dt> <dd>

Identificador de un proveedor de entradas de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pDevmode* \[ de\]
</dt> <dd>

Puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que se va a convertir.

</dd> <dt>

*cbSize* \[ de\]
</dt> <dd>

Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado en *pDevmode*.

</dd> <dt>

*ámbito* \[ de de\]
</dt> <dd>

Valor que especifica el ámbito de *ppPrintTicket*. Este valor puede especificar una sola página, un documento completo o todos los documentos en el trabajo de impresión. El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.

</dd> <dt>

*ppPrintTicket* \[ enuncia\]
</dt> <dd>

La dirección del búfer que contiene un vale de impresión que representa el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) pasado en *pDevmode*. Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer. Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintTicketLength* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, de la solicitud de impresión devuelta en *ppPrintTicket*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** . Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Imprimir esquema](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

