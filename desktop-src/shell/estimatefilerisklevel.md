---
description: Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y del contenido de código del archivo.
title: Función EstimateFileRiskLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841436"
---
# <a name="estimatefilerisklevel-function"></a>Función EstimateFileRiskLevel

\[Esta función está disponible en Windows XP con Service Pack 2 (SP2) a través de Windows Vista. Podría modificarse o no estar disponible en versiones posteriores de Windows. En su lugar, las aplicaciones cliente deben usar [**IAttachmentExecute para**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) presentar un entorno de usuario que proporciona descarga e intercambio seguro de archivos a través de correo electrónico y datos adjuntos de mensajería.\]

Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y del contenido de código del archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszFilePath* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en NULL que contiene la ruta de acceso del archivo que se comprueba con el controlador.

</dd> <dt>

*pszExt* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en NULL que contiene la extensión del archivo que se está compruebando, ya sea con o sin su período inicial. Por ejemplo, ".txt" o "txt".

</dd> <dt>

*pszHandler* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en NULL que contiene la ruta de acceso del controlador para el archivo.

</dd> <dt>

*pfrlEstimate* \[ out\]
</dt> <dd>

Tipo: **NIVEL DE RIESGO DE \_ \_ ARCHIVO \***

Cuando esta función se devuelve correctamente, contiene un puntero a uno de los valores siguientes que indica el riesgo estimado.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ SIN \_ OPINIÓN** (0)


</dt> <dd>

No se identifica el formato del archivo o no se identifica el controlador. Información insuficiente disponible para una respuesta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)


</dt> <dd>

El formato del archivo se entiende completamente, se conoce el controlador y hay una gran confianza en que no se ejecutará ningún código extraneous.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)


</dt> <dd>

Se identifica el formato del archivo, pero no se entiende lo suficiente para etiquetar como un riesgo alto o bajo.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)


</dt> <dd>

Se entiende el formato de archivo y se han identificado factores de riesgo elevados.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)


</dt> <dd>

El formato de archivo está bloqueado específicamente para este controlador.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función no se declara en un encabezado público ni se incluye en un archivo de biblioteca. Para usarlo, debe cargarlo directamente desde Winshfhc.dll ordinal 101.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio sp2 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Winshfhc.dll (versión 5.1 o posterior)</dt> </dl> |



 

 




