---
description: El método IWiaItem2::EnumRegisterEventInfo crea un enumerador que se puede usar para obtener información sobre los eventos para los que se registra una aplicación.
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: Método IWiaItem2::EnumRegisterEventInfo (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571333"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>IWiaItem2::EnumRegisterEventInfo (método)

El **método IWiaItem2::EnumRegisterEventInfo** crea un enumerador que se puede usar para obtener información sobre los eventos para los que se registra una aplicación.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

No se utiliza. Establecer en 0.

</dd> <dt>

*pEventGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Puntero a un identificador que especifica el evento de hardware para el que desea obtener información de registro.

</dd> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Dirección de un puntero a la [**interfaz \_ \_ CAPS de IEnumWIA DEV.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Una aplicación llama a este método para crear un objeto enumerador para la información del evento. **IWiaItem2::EnumRegisterEventInfo** almacena la dirección de la interfaz [**\_ \_ CAPS de IEnumWIA DEV**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) del objeto enumerador en el *parámetro ppIEnum.* A continuación, el programa usa el puntero de interfaz para enumerar las propiedades del evento para el que está registrado.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
