---
title: Método INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) según sea necesario para administrar la configuración remota directamente en el equipo especificado. Este método inicia una interfaz de usuario de administración de configuración.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Método InvokeUIForMachine NAP
- Método InvokeUIForMachine NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método InvokeUIForMachine
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
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150223"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>INapComponentConfig2:: InvokeUIForMachine (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **InvokeUIForMachine** según sea necesario para administrar la configuración remota directamente en el equipo especificado. Este método inicia una interfaz de usuario de administración de configuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Identificador de la ventana primaria o propietaria. Se debe proporcionar un identificador de ventana válido.

</dd> <dt>

*MachineName* \[ de\]
</dt> <dd>

Un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre de equipo del cliente NAP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





