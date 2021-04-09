---
description: 'El método IWiaItem2:: EnumRegisterEventInfo crea un enumerador que puede usar para obtener información sobre los eventos para los que se registra una aplicación.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2:: EnumRegisterEventInfo (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154401"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>IWiaItem2:: EnumRegisterEventInfo (método)

El método **IWiaItem2:: EnumRegisterEventInfo** crea un enumerador que puede usar para obtener información sobre los eventos para los que se registra una aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

No se utiliza. Establecer en 0.

</dd> <dt>

*pEventGUID* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

Puntero a un identificador que especifica el evento de hardware para el que desea obtener información de registro.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

La dirección de un puntero a la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Una aplicación llama a este método para crear un objeto de enumerador para la información de evento. **IWiaItem2:: EnumRegisterEventInfo** almacena la dirección de la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) del objeto enumerador en el parámetro *ppIEnum* . Después, el programa usa el puntero de interfaz para enumerar las propiedades del evento para el que se ha registrado.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
