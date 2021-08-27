---
title: Terminología del marco biométrico
description: Los siguientes términos se usan en la documentación Windows API de Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd88fe552d9a53d8bcf214280e5b15a9206532383afa87bfee6fe6dd95c9c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127265"
---
# <a name="biometric-framework-terminology"></a>Terminología del marco biométrico

Los siguientes términos se usan en la documentación Windows API de Biometric Framework.



| Término                                                 | Definición                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Marco biométrico (WBF)<br/>         | Una arquitectura de marco en Windows que proporciona una interfaz de administración coherente y una experiencia de usuario para dispositivos biométricos.<br/>                                                                                                                         |
| Servicio biométrico de Windows<br/>                 | Un servicio con privilegios que administra todos los dispositivos biométricos mediante Windows controladores de dispositivo compatibles con la Interfaz biométrica del controlador (WBDI).<br/>                                                                                                                   |
| Windows Interfaz del controlador biométrico<br/>        | Un estándar de interfaz para los controladores que administran sensores de huella digital.<br/>                                                                                                                                                                                     |
| Windows Proveedor de servicios biométricos (WBSP)<br/> | Componente del servicio biométrico Windows que administra una categoría específica de tecnología biométrica, como un lector de huellas digitales. Los WBSP están integrados en Windows Biometric Service. No son complementos y no se admiten BSP de terceros. <br/> |
| Factor biométrico<br/>                          | Característica personal que se puede medir y usar para la identificación. Algunos ejemplos son las huellas digitales y la geometría de la mano.<br/>                                                                                                                           |
| Subfactor biométrico<br/>                      | Característica que se puede usar para definir aún más un factor biométrico. Por ejemplo, para identificar completamente una huella digital (factor biométrico), es necesario especificar de qué dedo provenía la impresión (subfactor biométrico).<br/>             |
| Ejemplo biométrico<br/>                          | Datos que son el resultado de la medida de una sola característica de un solo individuo, por ejemplo, la imagen de una huella digital.<br/>                                                                                                              |
| Plantilla biométrica<br/>                        | Promedio estadístico generado mediante la recopilación de varias muestras biométricas de una sola característica para un solo individuo. Una plantilla suele contener únicamente las características necesarias para determinar si una muestra nueva concuerda.<br/>             |
| Unidad biométrica<br/>                            | Objeto de software que representa un dispositivo biométrico y se puede usar para capturar y procesar muestras biométricas y crear, guardar y hacer coincidir plantillas biométricas.<br/>                                                                                         |
| Adaptador de sensor<br/>                            | Un componente de complemento de unidad biométrica que proporciona una interfaz estándar para configurar el sensor, capturar muestras y controlar el flujo de datos biométricos al adaptador del motor.<br/>                                                                 |
| Adaptador de motor<br/>                            | Componente de complemento de unidad biométrica que procesa una muestra mediante la normalización de datos, la extracción de características y la coincidencia de datos de ejemplo con plantillas existentes.<br/>                                                                                                   |
| Adaptador de almacenamiento<br/>                           | Componente de complemento de unidad biométrica que almacena, administra y recupera plantillas.<br/>                                                                                                                                                                      |
| Registro de información biométrica (BIR)<br/>        | Estructura de datos que contiene información biométrica sin procesar o procesada.<br/>                                                                                                                                                                                 |
| Grupo de sensores<br/>                               | Colección de unidades biométricas que comparten una directiva de administración común.<br/>                                                                                                                                                                                 |
| Pruebas de vida<br/>                          | Un proceso que comprueba que una muestra biométrica no se suplanta ni se reproduce a partir de una muestra que se recopiló anteriormente.<br/>                                                                                                                          |



 

 

 





