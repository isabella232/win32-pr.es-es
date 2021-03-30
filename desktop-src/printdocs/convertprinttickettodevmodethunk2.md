---
description: Convierte una solicitud de impresión en una estructura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083025"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2 función)

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]

Convierte una solicitud de impresión en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ de\]
</dt> <dd>

Identificador de un proveedor de entradas de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pPrintTicket* \[ de\]
</dt> <dd>

Búfer que contiene el vale de impresión que se va a convertir.

</dd> <dt>

*cbSize* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer pasado en *pPrintTicket*.

</dd> <dt>

*BaseType* \[ de\]
</dt> <dd>

Un valor que indica si el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminado del usuario o el **DEVMODE** predeterminado de la cola de impresión se usa para proporcionar valores al **DEVMODE** de salida cuando *pPrintTicket* no especifica cada valor posible para una estructura **DEVMODE**. El valor de este parámetro debe ser un miembro de la enumeración [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , convertido en **int**.

</dd> <dt>

*ámbito* \[ de de\]
</dt> <dd>

Valor que especifica el ámbito de *pPrintTicket*. Este valor puede especificar una sola página, un documento completo o todos los documentos en el trabajo de impresión. El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.

</dd> <dt>

*ppDevmode* \[ enuncia\]
</dt> <dd>

Dirección del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)recién creado. Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer. Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbDevModeLength* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelto en *ppDevmode*.

</dd> <dt>

*errMsg* \[ out, opcional\]
</dt> <dd>

Un puntero a una cadena que especifica lo que, si hay alguna, no es válido sobre la solicitud de impresión en *pPrintTicket*. Si es válido, es **null**. Si *errMsg* no es **null** cuando la función devuelve, el llamador debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

