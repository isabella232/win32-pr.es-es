---
description: El monitor debe implementar el método configure. MCSVC llama a este método para obtener información de configuración de la captura.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: IMonitor::D método oConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154145"
---
# <a name="imonitordoconfigure-method"></a>IMonitor::D método oConfigure

El monitor debe implementar el método **Configure** . MCSVC llama a este método para obtener información de configuración de la captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Nombre de una instancia del monitor.

</dd> <dt>

*pConfiguration* \[ de\]
</dt> <dd>

Cadena de configuración proporcionada por MCSVC. El monitor debe analizar esta cadena para los datos de configuración.

</dd> <dt>

*ppScriptInstance* \[ enuncia\]
</dt> <dd>

Dirección de la cadena HTML utilizada para configurar el monitor. Si se usa un script predeterminado para la configuración, este valor debe establecerse en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es el mismo que NoError) y MCSVC ejecutará el monitor.

Si el método no se realiza correctamente, el valor devuelto es un código de error. Un valor devuelto de NMERR \_ monitor \_ config \_ no es aceptable, pero cuando se devuelve este error, el monitor no puede iniciarse hasta que se realice correctamente una llamada **configurada** en el futuro. Cualquier otro error impide que la instancia del monitor esté habilitada.

## <a name="remarks"></a>Observaciones

El MCSVC llama a este método después de que se haya conectado a la red y antes de que se llame al método [IRTC:: configure](irtc-configure.md) .

El monitor puede almacenar la información proporcionada por esta llamada, actualizar el script HTML o la cadena de configuración y establecer el [filtro de captura](capture-filters.md) en el BLOB NPP.

MCSVC puede llamar a este método varias veces, pero no se puede llamar mientras el monitor está capturando datos. Tenga en cuenta que cada vez que un [NPP](network-packet-providers.md) inicia una captura, se debe configurar la conexión a la red. Esta restricción incluye situaciones en las que se inicia NPP y detiene la misma captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




