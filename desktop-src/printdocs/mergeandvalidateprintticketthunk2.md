---
description: Combina dos vales de impresión y devuelve un vale de impresión válido y viable.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Función MergeAndValidatePrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 156a242d9aa017cc67106a39db6d86809e0ac6f464566205ead09f69fe1b3b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471687"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>Función MergeAndValidatePrintTicketThunk2

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTMergeAndValidatePrintTicket proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) una funcionalidad equivalente y se debe usar en su lugar.\]

Combina dos vales de impresión y devuelve un vale de impresión válido y viable.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ En\]
</dt> <dd>

Identificador de un proveedor de vales de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pBasePrintTicket* \[ En\]
</dt> <dd>

Búfer que contiene los datos del vale de impresión base, expresados en XML como se describe en [el esquema de impresión](./printschema.md).

</dd> <dt>

*basePrintTicketLength* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *pBasePrintTicket.*

</dd> <dt>

*pDeltaPrintTicket* \[ en, opcional\]
</dt> <dd>

Búfer que contiene el vale de impresión que se combinará. Los datos del vale de impresión se expresan en XML como se describe en [el esquema de impresión](./printschema.md). El valor de este parámetro puede ser **NULL.**

</dd> <dt>

*deltaPrintTicketLength* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *pDeltaPrintTicket.*

</dd> <dt>

*ámbito* \[ En\]
</dt> <dd>

Valor que especifica si el ámbito de *pDeltaPrintTicket* y *ppValidatedPrintTicket* es una sola página, un documento completo o todos los documentos del trabajo de impresión. El valor de este parámetro debe ser miembro de la enumeración [**EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) que se convierte como **DWORD.**

</dd> <dt>

*ppValidatedPrintTicket* \[ out\]
</dt> <dd>

Dirección del búfer que contiene el vale de impresión combinado y validado. Esta función llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar este búfer. Cuando el búfer ya no es necesario, el autor de la llamada debe liberarlo mediante una [**llamada a CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pValidatedPrintTicketLength* \[ out\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *ppValidatedPrintTicket.*

</dd> <dt>

*pbstrErrorMessage* \[ out, opcional\]
</dt> <dd>

Puntero a una cadena que especifica qué, si hay algo, no es válido sobre el vale de impresión en *pBasePrintTicket* o *pDeltaPrintTicket*. Si ambos son válidos, este valor es **NULL.** Si *pbstrErrorMessage* no es **NULL cuando** la función vuelve, el autor de la llamada debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error **HRESULT.** Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

