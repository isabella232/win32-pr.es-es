---
title: Función GetPhysicalMonitorDescription
description: Obtiene una descripción de un monitor físico.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configuración del monitor de la función GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251c24db32271802b94bd2beb7a381cc9b3adb50dd97842203947ea6a6895583
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534895"
---
# <a name="getphysicalmonitordescription-function"></a>Función GetPhysicalMonitorDescription

> [!IMPORTANT]
> Esta función la usa la API de configuración de monitor para acceder a la funcionalidad en el controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene una descripción de un monitor físico.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMonitor* \[ En\]
</dt> <dd>

Identificador de un monitor físico.

</dd> <dt>

*dwPhysicalMonitorDescriptionSizeInChars* \[ En\]
</dt> <dd>

Número de caracteres de la *matriz szPhysicalMonitorDescription.*

</dd> <dt>

*szPhysicalMonitorDescription* \[ out\]
</dt> <dd>

Puntero a una matriz que recibe la descripción. El número de elementos de la matriz debe ser al menos **PHYSICAL \_ MONITOR DESCRIPTION \_ \_ SIZE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Supervisar funciones de configuración](monitor-configuration-functions.md)
</dt> </dl>

 

