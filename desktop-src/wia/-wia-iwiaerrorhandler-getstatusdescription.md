---
description: Devuelve una cadena que describe el código de estado.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler:: GetStatusDescription (método) (WIA. h)'
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
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696616"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>IWiaErrorHandler:: GetStatusDescription (método)

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

*punkItem* \[ de\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntero a la [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir. Este objeto implementa mínimamente [_ *IWiaItem2* *](-wia-iwiaitem2.md) y [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ de\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que es el código de estado recibido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ de\]
</dt> <dd>

Tipo: **Long**

**Long** que es el tamaño de los datos a los que hace referencia *pbData*.

</dd> <dt>

*pbData* \[ de\]
</dt> <dd>

Tipo: **byte \** _

Puntero al búfer de datos tal y como lo recibe [_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*pbstrDescription* \[ enuncia\]
</dt> <dd>

Tipo: **BSTR \** _

_ *BSTR** que recibe una descripción del estado o error detectado durante la transferencia de datos. Este parámetro no puede ser **null**. El autor de la llamada debe liberar la cadena mediante [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)y el implementador debe asignar la cadena mediante [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve uno de los valores siguientes.



| Código devuelto                                                                             | Descripción                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | *pbstrDescription* contiene un puntero **BSTR** válido. <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *hrStatus* es desconocido y no hay ninguna descripción disponible. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
