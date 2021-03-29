---
title: Terminología de los marcos biométricos
description: Los siguientes términos se usan en la documentación de la API de Plataforma de biometría de Windows.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f150a30915a44dbd59a5a703577e79dc48933f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778984"
---
# <a name="biometric-framework-terminology"></a>Terminología de los marcos biométricos

Los siguientes términos se usan en la documentación de la API de Plataforma de biometría de Windows.



| Término                                                 | Definición                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plataforma de biometría de Windows (WBF)<br/>         | Arquitectura de marco de trabajo de Windows que proporciona una interfaz de administración y una experiencia de usuario coherentes para dispositivos biométricos.<br/>                                                                                                                         |
| Servicio biométrico de Windows<br/>                 | Un servicio con privilegios que administra todos los dispositivos biométricos mediante controladores de dispositivos compatibles con la interfaz de controlador biométrico de Windows (WBDI).<br/>                                                                                                                   |
| Interfaz del controlador biométrico de Windows<br/>        | Una interfaz estándar para los controladores que administran sensores de huellas digitales.<br/>                                                                                                                                                                                     |
| Proveedor de servicios biométricos de Windows (WBSP)<br/> | Componente del servicio biométrico de Windows que administra una categoría específica de tecnología biométrica, como un lector de huellas digitales. Los WBSPs están integrados en el servicio biométrico de Windows. No son complementos y no se admiten BSP de terceros. <br/> |
| Factor biométrico<br/>                          | Característica personal que se puede medir y usar para la identificación. Algunos ejemplos son las huellas digitales y la geometría de la mano.<br/>                                                                                                                           |
| Subfactor biométrico<br/>                      | Característica de calificación que se puede usar para definir aún más un factor biométrico. Por ejemplo, para identificar por completo una huella digital (factor biométrico) es necesario especificar el dedo del que procede la impresión (subfactor biométrico).<br/>             |
| Ejemplo biométrico<br/>                          | Los datos que son el resultado de la medición de una característica única de una sola persona, por ejemplo, la imagen de una huella digital.<br/>                                                                                                              |
| Plantilla biométrica<br/>                        | Promedio estadístico generado al recopilar varias muestras biométricas de una sola característica para una sola persona. Una plantilla suele contener únicamente las características necesarias para determinar si una muestra nueva concuerda.<br/>             |
| Unidad biométrica<br/>                            | Objeto de software que representa un dispositivo biométrico y se puede usar para capturar y procesar ejemplos biométricos y crear, guardar y hacer coincidir plantillas biométricas.<br/>                                                                                         |
| Adaptador de sensor<br/>                            | Componente de complemento de unidad biométrica que proporciona una interfaz estándar para configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al adaptador del motor.<br/>                                                                 |
| Adaptador de motor<br/>                            | Componente de complemento de unidad biométrica que procesa un ejemplo mediante la normalización de datos, la extracción de características y la coincidencia de datos de ejemplo con plantillas existentes.<br/>                                                                                                   |
| Adaptador de almacenamiento<br/>                           | Componente de complemento de unidad biométrica que almacena, administra y recupera plantillas.<br/>                                                                                                                                                                      |
| Registro de información biométrica (BIR)<br/>        | Una estructura de datos que contiene información biométrica sin procesar o procesada.<br/>                                                                                                                                                                                 |
| Grupo de sensores<br/>                               | Una colección de unidades biométricas que comparten una directiva de administración común.<br/>                                                                                                                                                                                 |
| Pruebas de vida<br/>                          | Proceso que comprueba que un ejemplo biométrico no se está suplantando o reproduciendo a partir de una muestra que se recopiló previamente.<br/>                                                                                                                          |



 

 

 





