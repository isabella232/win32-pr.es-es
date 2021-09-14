---
description: Obtiene los parámetros de configuración eapol para la interfaz LAN inalámbrica especificada.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Función WZCEapolGetInterfaceParams (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169394"
---
# <a name="wzceapolgetinterfaceparams-function"></a>Función WZCEapolGetInterfaceParams

\[**WZCEapolGetInterfaceParams** ya no se admite desde Windows Vista y Windows Server 2008. En su lugar, use [native Wifi API](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API de Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **función WZCEapolGetInterfaceParams** obtiene parámetros de configuración EAPOL para la interfaz LAN inalámbrica especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrvAddr* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **NULL,** se llama al servicio Configuración inalámbrica cero en el equipo local.

Si el *parámetro pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*pwszGuid* \[ En\]
</dt> <dd>

GUID de la interfaz para la que se recuperarán los datos.

</dd> <dt>

*dwSizeOfSSID* \[ En\]
</dt> <dd>

Tamaño del identificador de red para el que se recuperarán los datos.

</dd> <dt>

*pbSSID* \[ En\]
</dt> <dd>

Puntero al identificador de red para el que se recuperarán los datos.

</dd> <dt>

*pIntfParams* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**EAPOL \_ INTF \_ PARAMS**](eapol-intf-params.md) que contiene parámetros de interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve ERROR \_ SUCCESS si la operación se completa correctamente; de lo contrario, devuelve uno de los Windows de error del sistema.

## <a name="remarks"></a>Observaciones

Si **WZCEapolGetInterfaceParams** devuelve ERROR SUCCESS, el autor de la llamada debe llamar a LocalFree para liberar los búferes internos asignados para los datos devueltos una vez que esta información ya no sea \_ necesaria. [](/windows/win32/api/winbase/nf-winbase-localfree)

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* y el archivo de biblioteca de importación *Wzcsapi.lib* no están disponibles en Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                         |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
