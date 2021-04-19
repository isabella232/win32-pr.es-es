---
description: Especifica el tipo de acción de una operación de prevención de pérdida de datos (DLP) de punto de conexión.
title: Enumeración DlpActionType (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495955"
---
# <a name="dlpactiontype-enumeration"></a>Enumeración DlpActionType

Especifica el tipo de acción de una operación de prevención de pérdida de datos (DLP) del punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

Una operación de copia en un medio extraíble.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

Una operación de copia en una carpeta de red compartida.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

Una operación de copia en el Portapapeles.

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

Una operación de impresión.

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

Una operación de captura de pantalla.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

Una operación realizada por una aplicación no permitido.

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

Operación destinada a una ubicación en la nube.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

Una operación que incluye el acceso mediante una aplicación bluetooth.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

Una operación que incluye el acceso mediante un escritorio remoto.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

Valor máximo de la enumeración .

</dd> </dl>
 

## <a name="remarks"></a>Observaciones

La estructura DLP_APP_OP_ENLIGHTENED_LEVEL utiliza [los valores de esta enumeración.](endpointdlp-dlp_app_op_enlightened_level.md)

## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |

