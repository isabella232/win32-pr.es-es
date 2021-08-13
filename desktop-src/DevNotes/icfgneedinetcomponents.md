---
description: Determina si los componentes marcados en las opciones están instalados en el sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Función IcfgNeedInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 9b0d533e234986f54c6a4de668273bda08d9c810dc9f5a93acb3aaf030cea665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390665"
---
# <a name="icfgneedinetcomponents-function"></a>Función IcfgNeedInetComponents

Determina si los componentes marcados en las opciones están instalados en el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwfOptions* 
</dt> <dd>

Combinación de las marcas siguientes que especifican los componentes que se detectarán en la lista siguiente.



| Value                                                                                                                                                                                                                                  | Significado                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ InstallMAIL**</dt> <dt>0x00000004</dt> </dl> | ¿Exchange o correo electrónico de Internet?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | ¿Se necesita RAS?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | ¿Se necesita TCP/IP?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

Si este valor no es **NULL,** se devuelve **TRUE** si uno o varios componentes no están instalados en el sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Si no se produce ningún error, devuelve el **código ERROR \_ SUCCESS.**

## <a name="remarks"></a>Observaciones

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
