---
description: Emite un comando a un Windows de hardware de adquisición de imágenes (WIA) 2.0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: Método IWiaItem2::D eviceCommand (Wia.h)
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
ms.openlocfilehash: f70fd7b4a987dac3a079651f2cbc04dc50817ba8a43f8da1449a3f605683ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706315"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2::D eviceCommand (método)

Emite un comando a un Windows de hardware de adquisición de imágenes (WIA) 2.0.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*pCmdGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Especifica el comando que se enviará al dispositivo WIA 2.0. Consulte [**Comandos de dispositivo WIA**](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero al [**elemento IWiaItem2**](-wia-iwiaitem2.md) creado por el comando, si lo hay.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Además de los códigos de error COM estándar, el método puede devolver el siguiente valor.



| Código devuelto                                                                                       | Descripción                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | El comando no se implementa para la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) en la que se llama al método . El valor numérico de este error aún no está definido. <br/> |



 

## <a name="remarks"></a>Comentarios

El comportamiento de este método es diferente en función de la categoría del nodo en el que se llama al método.

Cuando la aplicación envía el comando [**WIA \_ CMD TAKE \_ \_ PICTURE**](-wia-wia-device-commands.md) al dispositivo mediante el método **IWiaItem2::D eviceCommand,** el sistema en tiempo de ejecución DE WIA 2.0 crea un objeto [**IWiaItem2**](-wia-iwiaitem2.md) para representar la imagen. El **método IWiaItem2::D eviceCommand** almacena la dirección de la interfaz en el *parámetro ppIWiaItem2.*

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
