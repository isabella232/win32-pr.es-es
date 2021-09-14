---
description: El experto debe implementar la función Run. Monitor de red llama a la función Run para iniciar al experto dentro del archivo DLL experto.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Ejecución de la función de devolución de llamada (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074083"
---
# <a name="run-callback-function"></a>Ejecución de la función de devolución de llamada

El experto debe implementar la **función Run.** Monitor de red llama a **la función Run** para iniciar al experto dentro del archivo DLL experto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único del experto que se devuelve a todas las funciones de Monitor de red expertos.

> [!Note]  
> El *identificador hEcialKey* puede pasar una clave de experto que sea diferente de la clave de experto que pasa la [**función**](configure.md) Configure.

 

</dd> <dt>

*pConfig* \[ En\]
</dt> <dd>

Puntero a la configuración existente. El *parámetro pConfig* puede ser **NULL,** lo que significa que el experto puede ejecutarse con valores predeterminados codificados de forma automática o información de inicio a la que hace referencia el parámetro *pE expertStartupInfo.*

</dd> <dt>

*pEcialStartupInfo* \[ En\]
</dt> <dd>

Puntero al elemento de captura que tiene el foco cuando se inicia el experto.

</dd> <dt>

*StartupFlags* \[ En\]
</dt> <dd>

Indicador de cómo el experto debe usar el *parámetro pE expertStartupInfo.*

La única marca definida es:



| Value                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**LA MARCA \_ DE INICIO EXPERTO USA DATOS DE INICIO SOBRE LOS DATOS DE \_ \_ \_ \_ \_ \_ \_ CONFIGURACIÓN.**</dt> </dl> | Esta marca indica que el experto usa el *parámetro pE expertStartupInfo* y no usa el *parámetro pConfig.* Normalmente, puede establecer esta marca cuando el experto puede empezar con un clic con el botón derecho del mouse. Si no se establece la marca, se pueden producir las dos cosas siguientes: el experto no se inicia con un clic con el botón derecho del mouse o el experto se inicia a partir de un clic con el botón derecho del mouse y, a continuación, el usuario lo configura.<br/> |



 

</dd> <dt>

*hWndParent* \[ En\]
</dt> <dd>

El *parámetro hWnd* del elemento primario (normalmente el Monitor de red interfaz de usuario).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, si se inicia el experto), el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Cuando se ejecuta, el experto recorre en bucle los fotogramas del archivo de captura y genera un informe o crea eventos que muestran problemas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




