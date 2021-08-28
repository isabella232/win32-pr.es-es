---
description: Convierte un vale de impresión en una estructura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Función ConvertPrintTicketToDevModeThunk2
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
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112685"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>Función ConvertPrintTicketToDevModeThunk2

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTConvertPrintTicketToDevMode proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) una funcionalidad equivalente y se debe usar en su lugar.\]

Convierte un vale de impresión en una [**estructura DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

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

*hProvider* \[ En\]
</dt> <dd>

Identificador de un proveedor de vales de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pPrintTicket* \[ En\]
</dt> <dd>

Búfer que contiene el vale de impresión que se convertirá.

</dd> <dt>

*cbSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer pasado *en pPrintTicket.*

</dd> <dt>

*baseType* \[ En\]
</dt> <dd>

Valor que indica si el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminado del usuario o el **DEVMODE** predeterminado de la cola de impresión se usa para proporcionar valores a **la salida DEVMODE** cuando *pPrintTicket* no especifica todos los valores posibles para **un DEVMODE**. El valor de este parámetro debe ser miembro de la enumeración [**EDefaultDevmodeType,**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) que se convierte como **int.**

</dd> <dt>

*ámbito* \[ En\]
</dt> <dd>

Valor que especifica el ámbito de *pPrintTicket.* Este valor puede especificar una sola página, un documento completo o todos los documentos del trabajo de impresión. El valor de este parámetro debe ser miembro de la enumeración [**EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) que se convierte como **DWORD.**

</dd> <dt>

*ppDevmode* \[ out\]
</dt> <dd>

Dirección del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)recién creado. Esta función llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar este búfer. Cuando el búfer ya no es necesario, el autor de la llamada debe liberarlo mediante una [**llamada a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*devModeLength* \[ out\]
</dt> <dd>

Tamaño, en bytes, del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelto en *ppDevmode*.

</dd> <dt>

*errMsg* \[ out, opcional\]
</dt> <dd>

Puntero a una cadena que especifica qué, si hay algo, no es válido sobre el vale de impresión en *pPrintTicket*. Si es válido, es **NULL.** Si *errMsg* no es **NULL cuando** la función vuelve, el autor de la llamada debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error **HRESULT.** Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

