---
description: Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 función)
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
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688576"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2 función)

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]

Combina dos solicitudes de impresión y devuelve una solicitud de impresión válida y viable.

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

*hProvider* \[ de\]
</dt> <dd>

Identificador de un proveedor de entradas de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

</dd> <dt>

*pBasePrintTicket* \[ de\]
</dt> <dd>

Búfer que contiene los datos de los vales de impresión base, expresados en XML, tal como se describe en el [esquema de impresión](./printschema.md).

</dd> <dt>

*basePrintTicketLength* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *pBasePrintTicket*.

</dd> <dt>

*pDeltaPrintTicket* \[ en, opcional\]
</dt> <dd>

Búfer que contiene el vale de impresión que se va a combinar. Los datos de los vales de impresión se expresan en XML tal y como se describe en el [esquema de impresión](./printschema.md). El valor de este parámetro puede ser **null**.

</dd> <dt>

*deltaPrintTicketLength* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *pDeltaPrintTicket*.

</dd> <dt>

*ámbito* \[ de de\]
</dt> <dd>

Valor que especifica si el ámbito de *pDeltaPrintTicket* y *ppValidatedPrintTicket* es una sola página, un documento completo o todos los documentos en el trabajo de impresión. El valor de este parámetro debe ser un miembro de la enumeración [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , convertido en **DWORD**.

</dd> <dt>

*ppValidatedPrintTicket* \[ enuncia\]
</dt> <dd>

La dirección del búfer que contiene la solicitud de impresión combinada y validada. Esta función llama a [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar este búfer. Cuando el búfer ya no se necesita, el llamador debe liberarlo llamando a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pValidatedPrintTicketLength* \[ enuncia\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *ppValidatedPrintTicket*.

</dd> <dt>

*pbstrErrorMessage* \[ out, opcional\]
</dt> <dd>

Un puntero a una cadena que especifica lo que, si hay alguna, no es válido sobre la solicitud de impresión en *pBasePrintTicket* o *pDeltaPrintTicket*. Si ambos son válidos, este valor es **null**. Si *pbstrErrorMessage* no es **null** cuando la función devuelve, el llamador debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

