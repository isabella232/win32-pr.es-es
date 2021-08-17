---
description: Instala los componentes del sistema especificados.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Función IcfgInstallInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827291"
---
# <a name="icfginstallinetcomponents-function"></a>Función IcfgInstallInetComponents

Instala los componentes del sistema especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* 
</dt> <dd>

Identificador de la ventana primaria.

</dd> <dt>

*dwfOptions* 
</dt> <dd>

Combinación de las marcas siguientes que controlan la instalación y la configuración.



| Valor                                                                                                                                                                                                                                  | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ InstallMAIL**</dt> <dt>0x00000004</dt> </dl> | Instale Exchange correo electrónico de Internet.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ InstallRAS**</dt> <dt>0x00000002</dt> </dl>    | Instale RAS (si es necesario).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ InstallTCP**</dt> <dt>0x00000001</dt> </dl>    | Instale TCP/IP (si es necesario).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Si este valor no es **NULL,** al devolverlo será **TRUE** solo si Windows debe reiniciarse para completar la instalación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Si no se produce ningún error, devuelve el **código ERROR \_ SUCCESS.**

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
