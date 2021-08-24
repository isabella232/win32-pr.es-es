---
description: El monitor debe implementar el método DoConfigure. MCSVC llama a este método para obtener información de configuración para la captura.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Método IMonitor::D oConfigure (Netmon.h)
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
ms.openlocfilehash: 9776ca62cbb61b6708f00d5e1d6d85eeab245b32798683b5afde546d835633c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779195"
---
# <a name="imonitordoconfigure-method"></a>IMonitor::D oConfigure (método)

El monitor debe implementar el método **DoConfigure.** MCSVC llama a este método para obtener información de configuración para la captura.

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

*pName* \[ En\]
</dt> <dd>

Nombre de una instancia del monitor.

</dd> <dt>

*pConfiguration* \[ En\]
</dt> <dd>

Cadena de configuración proporcionada por MCSVC. El monitor debe analizar esta cadena para los datos de configuración.

</dd> <dt>

*ppScriptInstance* \[ out\]
</dt> <dd>

Dirección de la cadena HTML utilizada para configurar el monitor. Si se usa un script predeterminado para la configuración, este valor debe establecerse en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S OK (que es igual \_ que NOERROR) y MCSVC ejecutará el monitor.

Si el método no es correcto, el valor devuelto es un código de error. Se acepta un valor devuelto de error de configuración de NMERR MONITOR, pero cuando se devuelve este error, el monitor no se puede iniciar hasta que una llamada \_ \_ a \_ **DoConfigure** futura se realice correctamente. Cualquier otro error impide que se habilite la instancia del monitor.

## <a name="remarks"></a>Comentarios

MCSVC llama a este método después de conectarse a la red y antes de llamar al método [IRTC::Configure.](irtc-configure.md)

El monitor puede almacenar la información proporcionada por esta llamada, actualizar el script HTML o la cadena de configuración y establecer el filtro de captura [en](capture-filters.md) el blob de NPP.

MCSVC puede llamar a este método varias veces, pero no se puede llamar mientras el monitor captura datos. Tenga en cuenta que cada vez [que un NPP](network-packet-providers.md) inicia una captura, se debe configurar la conexión a la red. Esta restricción incluye situaciones en las que el NPP inicia y detiene la misma captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




