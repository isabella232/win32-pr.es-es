---
description: Recupera las funcionalidades de impresoras con formato conforme al esquema de impresión XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: Función GetPrintCapabilitiesThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 55127d15eae41380fd5376ca54589488e255a740a7881042f54bc203873701f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971394"
---
# <a name="getprintcapabilitiesthunk2-function"></a>Función GetPrintCapabilitiesThunk2

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTGetPrintCapabilities proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) una funcionalidad equivalente y se debe usar en su lugar.\]

Recupera las funciones de la impresora con formato conforme al esquema [de impresión](./printschema.md)XML .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
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

Búfer que contiene los datos del vale de impresión, expresados en XML como se describe en [el esquema de impresión](./printschema.md).

</dd> <dt>

*cbPrintTicket* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *pPrintTicket.*

</dd> <dt>

*ppbPrintCapabilities* \[ out\]
</dt> <dd>

Dirección del búfer asignado por esta función y que contiene la información de las funcionalidades de impresión válidas, codificadas como XML. Esta función llama [**a CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) asignar este búfer. Cuando el búfer ya no es necesario, el autor de la llamada debe liberarlo llamando a [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*printPrintCapabilitiesLength* \[ out\]
</dt> <dd>

Tamaño, en bytes, del búfer al que hace referencia *ppbPrintCapabilities.*

</dd> <dt>

*pbstrErrorMessage* \[ out, opcional\]
</dt> <dd>

Puntero a una cadena que especifica qué, si hay algo, no es válido sobre *pPrintTicket.* Si es válido, este valor es **NULL.** Si *pbstrErrorMessage* no es **NULL cuando** la función vuelve, el autor de la llamada debe liberar la cadena con [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error **HRESULT.** Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

