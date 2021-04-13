---
description: Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y el contenido del código del archivo.
title: EstimateFileRiskLevel función)
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
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985903"
---
# <a name="estimatefilerisklevel-function"></a>EstimateFileRiskLevel función)

\[Esta función está disponible en Windows XP con Service Pack 2 (SP2) a través de Windows Vista. Podría modificarse o no estar disponible en versiones posteriores de Windows. En su lugar, las aplicaciones cliente deben usar [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) para presentar un entorno de usuario que proporcione descarga e intercambio seguro de archivos a través de mensajes de correo electrónico y datos adjuntos.\]

Calcula el riesgo de ejecutar código desconocido cuando se llama a un controlador en un archivo determinado. Este riesgo se basa en una comprensión del controlador y el contenido del código del archivo.

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

*pszFilePath* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero a una cadena terminada en null que contiene la ruta de acceso del archivo que se va a comprobar en el controlador.

</dd> <dt>

*pszExt* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Un puntero a una cadena terminada en null que contiene la extensión del archivo que se está comprobando, con o sin el punto inicial. Por ejemplo, ". txt" o "txt".

</dd> <dt>

*pszHandler* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Un puntero a una cadena terminada en null que contiene la ruta de acceso del controlador del archivo.

</dd> <dt>

*pfrlEstimate* \[ enuncia\]
</dt> <dd>

Tipo: **\_ \_ nivel \* de riesgo de archivo* _

Cuando esta función se devuelve correctamente, contiene un puntero a uno de los valores siguientes que indican el riesgo estimado.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ sin \_ opinión** (0)


</dt> <dd>

El formato del archivo no está identificado o el controlador no está identificado. No hay información disponible para una respuesta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ BAJO** (1)


</dt> <dd>

El formato del archivo se entiende por completo, se conoce el controlador y hay mucha confianza de que no se ejecutará ningún código extraño.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERADO** (2)


</dt> <dd>

Se identifica el formato del archivo, pero no se entiende lo suficientemente como como riesgo alto o bajo.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTO** (3)


</dt> <dd>

Se entiende el formato de archivo y se han identificado los factores de riesgo elevados.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOQUE** (4)


</dt> <dd>

El formato de archivo está bloqueado específicamente para este controlador.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función no se declara en un encabezado público o se incluye en un archivo de biblioteca. Para usarlo, debe cargarlo directamente desde Winshfhc.dll por el ordinal 101.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Winshfhc.dll (versión 5,1 o posterior)</dt> </dl> |



 

 




