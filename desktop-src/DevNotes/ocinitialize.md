---
description: Inicializa el administrador de componentes opcional.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize función)
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
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649627"
---
# <a name="ocinitialize-function"></a>OcInitialize función)

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

*Devoluciones de llamada* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ devoluciones de llamada de cliente de OCM**](ocm-client-callbacks.md) que especifica las funciones de devolución de llamada que va a usar el administrador de OC para realizar varias tareas.

</dd> <dt>

*MasterOcInfName* \[ de\]
</dt> <dd>

Ruta de acceso del archivo. inf de procesamiento maestro.

</dd> <dt>

*Flags* \[in\]
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

*ShowError* \[ enuncia\]
</dt> <dd>

Si se produce un error en la función, este parámetro indica si se muestra un mensaje de error.

</dd> <dt>

*Registro* \[ de de\]
</dt> <dd>

Identificador del registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el valor de contexto del administrador de OC.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_devoluciones de llamada de cliente de OCM \_**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
