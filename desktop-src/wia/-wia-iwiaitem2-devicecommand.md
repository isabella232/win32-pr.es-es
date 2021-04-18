---
description: Emite un comando para un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2::D método eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715195"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2::D método eviceCommand

Emite un comando para un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pCmdGUID* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica el comando que se va a enviar al dispositivo WIA 2,0. Consulte [_ *comandos* * de dispositivo WIA](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero al elemento [**IWiaItem2**](-wia-iwiaitem2.md) creado por el comando, si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Además de los códigos de error COM estándar, el método puede devolver el valor siguiente.



| Código devuelto                                                                                       | Descripción                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | El comando no está implementado para la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) en la que se llama al método. El valor numérico de este error aún no se ha definido. <br/> |



 

## <a name="remarks"></a>Observaciones

El comportamiento de este método es diferente en función de la categoría del nodo en el que se llama al método.

Cuando la aplicación envía el comando [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) al dispositivo mediante el método **IWiaItem2::D evicecommand** , el sistema en tiempo de ejecución de WIA 2,0 crea un objeto [**IWiaItem2**](-wia-iwiaitem2.md) para representar la imagen. El método **IWiaItem2::D evicecommand** almacena la dirección de la interfaz en el parámetro *ppIWiaItem2* .

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
