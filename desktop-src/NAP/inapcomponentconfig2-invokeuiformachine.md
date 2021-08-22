---
title: Método INapComponentConfig2 InvokeUIForMachine (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) según sea necesario para administrar la configuración remota directamente en la máquina especificada. Este método inicia una interfaz de usuario de administración de configuración.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Nap del método InvokeUIForMachine
- Interfaz NAP del método InvokeUIForMachine , INapComponentConfig2
- Nap de interfaz INapComponentConfig2, método InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940193"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>Método INapComponentConfig2::InvokeUIForMachine

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **InvokeUIForMachine** según sea necesario para administrar la configuración remota directamente en la máquina especificada. Este método inicia una interfaz de usuario de administración de configuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Identificador de la ventana principal o del propietario. Se debe proporcionar un identificador de ventana válido.

</dd> <dt>

*machineName* \[ En\]
</dt> <dd>

Puntero a [**countedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del equipo del cliente NAP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o uno de los códigos de error Windows estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





