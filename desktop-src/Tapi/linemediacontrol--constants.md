---
description: Las \_ constantes de marcador de bits LINEMEDIACONTROL describen un conjunto de operaciones genéricas en flujos multimedia.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Constantes de LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690698"
---
# <a name="linemediacontrol_-constants"></a>Constantes de LINEMEDIACONTROL \_

Las constantes de marcador de bits **LINEMEDIACONTROL \_** describen un conjunto de operaciones genéricas en flujos multimedia. La secuencia de medios determina las interpretaciones. El dispositivo de línea debe tener la capacidad de control de medios para que cualquier operación de control de medios sea efectiva.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ ninguno**
</dt> <dd> <dl> <dt>



No se realiza ningún cambio en el flujo multimedia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**pausar LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Detenga temporalmente el flujo multimedia.

La velocidad del flujo multimedia se devuelve a la normalidad.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



La velocidad de la secuencia de medios disminuye en función de la cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



La velocidad de la secuencia de medios aumenta en función de la cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**restablecimiento de LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Restablezca el flujo multimedia. Equivalente a un final de entrada. Se liberan todos los búferes.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**\_reanudación de LINEMEDIACONTROL**
</dt> <dd> <dl> <dt>



Reanudar una secuencia de medios en pausa.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**Inicio de LINEMEDIACONTROL \_**
</dt> <dd> <dl> <dt>



Inicie el flujo multimedia.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



La amplitud de la secuencia multimedia disminuye en función de la cantidad definida por el flujo.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



La amplitud del flujo multimedia se devuelve a normal.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



La amplitud de la secuencia de medios aumenta en función de la cantidad definida por el flujo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

El control multimedia se proporciona para mejorar el rendimiento de las acciones en flujos multimedia en respuesta a eventos relacionados con la telefonía. Normalmente, la aplicación debe administrar un flujo de medios a través de la API específica del medio. La funcionalidad de control de medios que se proporciona aquí no está pensada para reemplazar las API multimedia nativas.

Las acciones de control de medios pueden asociarse con la detección de dígitos, la detección de tonos, la transición a un estado de llamada y la detección de un tipo de medio. Consulte las funciones de los dispositivos de una línea para determinar si el control multimedia está disponible en la línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




