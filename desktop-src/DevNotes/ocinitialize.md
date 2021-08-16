---
description: Inicializa el administrador de componentes opcional.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Función OcInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 08e7ffd7f8ad6faa2b08f937627627b6e74bbc09505482c589023db5dae37677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826750"
---
# <a name="ocinitialize-function"></a>Función OcInitialize

Inicializa el administrador de componentes opcional.

## <a name="syntax"></a>Sintaxis


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Devoluciones de llamada* \[ En\]
</dt> <dd>

Puntero a una estructura [**OCM \_ CLIENT \_ CALLBACKS**](ocm-client-callbacks.md) que especifica las funciones de devolución de llamada que el administrador de OC usará para realizar varias tareas.

</dd> <dt>

*MasterOcInfName* \[ En\]
</dt> <dd>

Ruta de acceso del archivo OC .inf maestro.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ out\]
</dt> <dd>

Si se produce un error en la función, este parámetro indica si se debe mostrar un mensaje de error.

</dd> <dt>

*Registro* \[ En\]
</dt> <dd>

Identificador del registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el valor de contexto del administrador de OC.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DEVOLUCIONES DE LLAMADA \_ DE CLIENTE DE OCM \_**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
