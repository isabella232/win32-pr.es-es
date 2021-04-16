---
title: IWMPSettings2 requestMediaAccessRights, método
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | IWMPSettings2 requestMediaAccessRights, método
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- método requestMediaAccessRights de Windows Media Player
- método requestMediaAccessRights Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690420"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2:: requestMediaAccessRights (método)

El método **requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDesiredAccess* \[ de\]
</dt> <dd>

**System. String** que es uno de los valores siguientes.



| Value | Descripción                      |
|-------|----------------------------------|
| ninguno  | Solo los derechos de acceso a elementos actuales. |
| leer  | Solo derechos de acceso de lectura.         |
| full  | Derechos de acceso de lectura y escritura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Boolean** que indica si se han concedido los derechos de acceso solicitados.

## <a name="remarks"></a>Observaciones

Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca. Al invocar este método, se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes. El nivel de derechos de acceso actual se puede recuperar mediante **IWMPSettings2. mediaAccessRights**.

No es necesario que las aplicaciones que se ejecutan en el equipo del usuario utilicen este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





