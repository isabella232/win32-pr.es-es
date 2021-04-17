---
description: Cierra un identificador de un proveedor de entradas de impresión.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697150"
---
# <a name="unbindptproviderthunk-function"></a>UnbindPTProviderThunk función)

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) proporciona una funcionalidad equivalente y se debe usar en su lugar.\]

Cierra un identificador de un proveedor de entradas de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ de\]
</dt> <dd>

Identificador de un proveedor de entradas de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

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

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

