---
description: Abre una instancia de un proveedor de vales de impresión.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Función BindPTProviderThunk
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
ms.openlocfilehash: 460728eac742fb96ca122981a5874408e12e6c8eddd36fc901e70874e5e040c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720235"
---
# <a name="bindptproviderthunk-function"></a>Función BindPTProviderThunk

\[Esta función no se admite y podría deshabilitarse o eliminarse en versiones futuras de Windows. [**PTOpenProviderEx proporciona**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) una funcionalidad equivalente y se debe usar en su lugar.\]

Abre una instancia de un proveedor de vales de impresión.

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

*pszPrinterName* \[ En\]
</dt> <dd>

Nombre completo de una cola de impresión.

</dd> <dt>

*maxVersion* \[ En\]
</dt> <dd>

La versión más reciente del [esquema de impresión que](./printschema.md) admite el autor de la llamada.

</dd> <dt>

*prefVersion* \[ En\]
</dt> <dd>

Versión del esquema de [impresión solicitada](./printschema.md) por el autor de la llamada.

</dd> <dt>

*phProvider* \[ out\]
</dt> <dd>

Puntero a un identificador al proveedor de vales de impresión.

</dd> <dt>

*usedVersion* \[ out\]
</dt> <dd>

Versión del esquema de [impresión que](./printschema.md) usará el proveedor de vales de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK;** de lo contrario, devuelve un código de error **HRESULT.** Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

Antes de llamar a esta función, el subproceso que realiza la llamada debe inicializar COM mediante [**una llamada a CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

