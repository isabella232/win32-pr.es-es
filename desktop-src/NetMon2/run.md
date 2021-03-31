---
description: El experto debe implementar la función de ejecución. Monitor de red llama a la función Run para iniciar el experto en el archivo DLL de expertos.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Ejecutar función de devolución de llamada (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908115"
---
# <a name="run-callback-function"></a>Ejecutar función de devolución de llamada

El experto debe implementar la función de **ejecución** . Monitor de red llama a la función **Run** para iniciar el experto en el archivo dll de expertos.

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

*hExpertKey* \[ de\]
</dt> <dd>

Identificador único del experto que se pasa de nuevo a todas las funciones de Monitor de red específicas del experto.

> [!Note]  
> El identificador *hExpertKey* puede pasar una clave experta que sea diferente de la clave experta que pasa la función [**Configure**](configure.md) .

 

</dd> <dt>

*pConfig* \[ de\]
</dt> <dd>

Puntero a la configuración existente. El parámetro *pConfig* puede ser **null** , lo que significa que el experto puede ejecutarse con valores predeterminados codificados de forma rígida o con información de inicio a la que hace referencia el parámetro *pExpertStartupInfo* .

</dd> <dt>

*pExpertStartupInfo* \[ de\]
</dt> <dd>

Puntero al elemento de captura que tiene el foco cuando se inicia el experto.

</dd> <dt>

*StartupFlags* \[ de\]
</dt> <dd>

Indicador de cómo el experto debe usar el parámetro *pExpertStartupInfo* .

La única marca definida es:



| Value                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**marca de inicio de experto \_ \_ \_ use \_ datos de inicio \_ \_ sobre \_ datos de configuración \_ .**</dt> </dl> | Esta marca indica que el experto usa el parámetro *pExpertStartupInfo* y no usa el parámetro *pConfig* . Normalmente, puede establecer esta marca cuando el experto puede empezar con un clic con el botón secundario del mouse. Si no se establece la marca, pueden producirse las dos cosas siguientes: el experto no se inicia con un clic con el botón derecho, o el experto comienza con un clic con el botón secundario y, a continuación, el usuario lo configura.<br/> |



 

</dd> <dt>

*hWndParent* \[ de\]
</dt> <dd>

Parámetro *hWnd* del elemento primario (normalmente la interfaz de usuario monitor de red).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si se inicia el experto), el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Al ejecutar, el experto crea un bucle a través de los fotogramas del archivo de captura y genera un informe o los eventos que muestran problemas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




