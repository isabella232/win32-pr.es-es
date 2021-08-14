---
description: Las constantes de marca de bits LINEMEDIACONTROL \_ describen un conjunto de operaciones genéricas en secuencias multimedia.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: LINEMEDIACONTROL_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309975"
---
# <a name="linemediacontrol_-constants"></a>LineMEDIACONTROL \_ (constantes)

Las constantes de marca de bits **LINEMEDIACONTROL \_** describen un conjunto de operaciones genéricas en secuencias multimedia. Las interpretaciones las determina la secuencia multimedia. El dispositivo de línea debe tener la funcionalidad de control multimedia para que cualquier operación de control multimedia sea eficaz.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ NONE**
</dt> <dd> <dl> <dt>



No se debe realizar ningún cambio en la secuencia multimedia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ PAUSE**
</dt> <dd> <dl> <dt>



Pausa temporalmente la secuencia multimedia.

La velocidad de la secuencia multimedia se devuelve a la normalidad.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



La velocidad de la secuencia multimedia se reduce en alguna cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



La velocidad del flujo multimedia aumenta en alguna cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL \_ RESET**
</dt> <dd> <dl> <dt>



Restablezca la secuencia multimedia. Equivalente a un final de entrada. Se liberan todos los búferes.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ RESUME**
</dt> <dd> <dl> <dt>



Reanude una secuencia multimedia en pausa.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ START**
</dt> <dd> <dl> <dt>



Inicie el flujo multimedia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



La amplitud de la secuencia multimedia se reduce en alguna cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



La amplitud de la secuencia multimedia se devuelve a la normalidad.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



La amplitud de la secuencia multimedia aumenta en alguna cantidad definida por el flujo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

El control multimedia se proporciona para mejorar el rendimiento de las acciones en secuencias multimedia en respuesta a eventos relacionados con la telefonía. Normalmente, la aplicación debe administrar un flujo multimedia a través de la API específica del medio. La funcionalidad de control multimedia que se proporciona aquí no está pensada para reemplazar las API de medios nativos.

Las acciones de control multimedia se pueden asociar con la detección de dígitos, la detección de tonos, la transición a un estado de llamada y la detección de un tipo de medio. Consulte las funcionalidades del dispositivo de una línea para determinar si el control multimedia está disponible en la línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




