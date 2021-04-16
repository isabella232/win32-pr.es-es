---
description: Instala los componentes del sistema especificados.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents función)
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
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649787"
---
# <a name="icfginstallinetcomponents-function"></a>IcfgInstallInetComponents función)

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



| Value                                                                                                                                                                                                                                  | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | Instale Exchange y correo de Internet.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | Instalar RAS (si es necesario).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Instale TCP/IP (si es necesario).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Si este valor no es **null**, en la devolución solo será **true** si Windows debe reiniciarse para completar la instalación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Si no se produce ningún error, devuelve el código de **error \_ correcto** .

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
