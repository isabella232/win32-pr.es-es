---
title: Propiedad mediaAccessRights de IWMPSettings2
description: La propiedad mediaAccessRights obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- propiedades de mediaAccessRights Media Player de Windows
- propiedad mediaAccessRights de Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, propiedad mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689940"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>IWMPSettings2:: mediaAccessRights (propiedad)

La propiedad **mediaAccessRights** obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es uno de los valores siguientes.



| Value | Descripción                      |
|-------|----------------------------------|
| ninguno  | Solo los derechos de acceso a elementos actuales. |
| leer  | Solo derechos de acceso de lectura.         |
| full  | Derechos de acceso de lectura y escritura.        |



 

## <a name="remarks"></a>Observaciones

Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca. Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes. Para obtener derechos de acceso, la aplicación llama a **IWMPSettings2. Get \_ requestMediaAccessRights**, pasando un parámetro que especifica el nivel de derechos de acceso deseado.

Las aplicaciones que se ejecutan en el equipo del usuario siempre tienen derechos de acceso completo.

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

[**IWMPSettings2. requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





