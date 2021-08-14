---
description: Devuelve una cadena que describe el código de estado.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: Método IWiaErrorHandler::GetStatusDescription (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208307"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>IWiaErrorHandler::GetStatusDescription (método)

Devuelve una cadena que describe el código de estado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itemitem* \[ En\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero al [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir. Este objeto implementa mínimamente [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ En\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que es el código de estado recibido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ En\]
</dt> <dd>

Tipo: **LONG**

**LONG** que es el tamaño de los datos a los que hace referencia *pbData.*

</dd> <dt>

*pbData* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero al búfer de datos recibido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*pbstrDescription* \[ out\]
</dt> <dd>

Tipo: **BSTR \***

**BSTR** que recibe una descripción del estado o error detectado durante la transferencia de datos. Este parámetro no puede ser **NULL.** El autor de la llamada debe liberar la cadena [mediante SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)y el implementador debe asignar la cadena [mediante SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve uno de los valores siguientes.



| Código devuelto                                                                             | Descripción                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstrDescription* contiene un puntero **BSTR** válido. <br/>  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *hrStatus* es desconocido y no hay ninguna descripción disponible. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
