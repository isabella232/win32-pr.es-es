---
description: Cierra un identificador a un proveedor de vales de impresión.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Función UnbindPTProviderThunk
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
ms.openlocfilehash: e9091360a34a00b7598e50c1b3226d8cc82c82f124602b0308836c61dc8f27ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686001"
---
# <a name="unbindptproviderthunk-function"></a>Función UnbindPTProviderThunk

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTCloseProvider proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) una funcionalidad equivalente y se debe usar en su lugar.\]

Cierra un identificador a un proveedor de vales de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* \[ En\]
</dt> <dd>

Identificador de un proveedor de vales de impresión abierto. La función [**BindPTProviderThunk**](bindptproviderthunk.md) devuelve este identificador.

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

[Esquema de impresión](./printschema.md)
</dt> <dt>

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

