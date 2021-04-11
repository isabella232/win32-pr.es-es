---
description: Abre una instancia de un proveedor de entradas de impresión.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276670"
---
# <a name="bindptproviderthunk-function"></a>BindPTProviderThunk función)

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]

Abre una instancia de un proveedor de entradas de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPrinterName* \[ de\]
</dt> <dd>

Nombre completo de una cola de impresión.

</dd> <dt>

*MaxVersion* \[ de\]
</dt> <dd>

La versión más reciente del [esquema de impresión](./printschema.md) que admite el autor de la llamada.

</dd> <dt>

*prefVersion* \[ de\]
</dt> <dd>

Versión del esquema de [impresión](./printschema.md) solicitado por el autor de la llamada.

</dd> <dt>

*phProvider* \[ enuncia\]
</dt> <dd>

Un puntero a un identificador para el proveedor de entradas de impresión.

</dd> <dt>

*usedVersion* \[ enuncia\]
</dt> <dd>

Versión del esquema de [impresión](./printschema.md) que utilizará el proveedor de entradas de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error **HRESULT** . Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

Antes de llamar a esta función, el subproceso que realiza la llamada debe inicializar COM llamando a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

