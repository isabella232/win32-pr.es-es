---
title: Método IWMPSettings2 requestMediaAccessRights
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | Método IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Método requestMediaAccessRights Reproductor de Windows Media
- Método requestMediaAccessRights Reproductor de Windows Media , interfaz IWMPSettings2
- Interfaz IWMPSettings2 Reproductor de Windows Media , método requestMediaAccessRights
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
ms.openlocfilehash: aba44540717059945f273be23d2e3c63b3c10cfc6d21d35ee1c4756ea1503708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568492"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2::requestMediaAccessRights (método)

El **método requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.

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

*bstrDesiredAccess* \[ En\]
</dt> <dd>

**System.String que** es uno de los valores siguientes.



| Valor | Descripción                      |
|-------|----------------------------------|
| ninguno  | Solo derechos de acceso de elementos actuales. |
| leer  | Solo derechos de acceso de lectura.         |
| full  | Derechos de acceso de lectura y escritura.        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Boolean que** indica si se han concedido los derechos de acceso solicitados.

## <a name="remarks"></a>Comentarios

Una página web debe solicitar primero permiso al usuario para leer información o escribir datos en la biblioteca. Al invocar este método, se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso adecuados. El nivel de derechos de acceso actual se puede recuperar mediante **IWMPSettings2.mediaAccessRights**.

Las aplicaciones que se ejecutan en el equipo del usuario no son necesarias para usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





