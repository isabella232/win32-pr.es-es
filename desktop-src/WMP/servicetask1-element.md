---
title: Elemento ServiceTask1
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento ServiceTask1 representa el primer panel de tareas de la tienda en línea.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- Elemento ServiceTask1 Media Player Windows
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649821"
---
# <a name="servicetask1-element"></a>Elemento ServiceTask1

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **ServiceTask1** representa el primer panel de tareas de la tienda en línea.

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                             | Descripción                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatorio)<br/> | Dirección URL de la página web que Windows Media Player muestra.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento                       |
|-----------------|-------------------------------|
| Elementos primarios | **ServiceInfo**               |
| Elementos secundarios  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Observaciones

**ServiceTask1** se considera el panel de tareas principal para participar en la actividad comercial. Es el panel de tareas que se muestra cuando el usuario elige comprar música.

> [!Note]  
> Windows Media Player 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas Web. La tienda en línea puede elegir usar uno, dos o los tres paneles de tareas. Windows Media Player 11 solo tiene un panel de tareas, representado por **ServiceTask1**, que el usuario puede ver haciendo clic en la pestaña **tiendas en línea** .

 

Los paneles de tareas de la tienda en línea comparten una única instancia del explorador. Esto significa que no debe escribir código de script en la página web que espera que continúe ejecutándose cuando el usuario cambia de la tarea de servicio actual.

Cuando el usuario cambia los paneles de tareas, Windows Media Player almacena las cookies de la dirección URL y la sesión. Cuando el usuario vuelve al panel de tareas, el reproductor restaura la dirección URL y las cookies. Si el usuario elige usar una tienda en línea diferente, se borran los datos de la dirección URL y la sesión.

En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL. Otros pueden estar presentes para fines de compatibilidad heredada.



| Nombre         | Value                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | IDENTIFICADOR de ubicación geográfica de Windows. El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control. |
| *locale*     | IDENTIFICADOR de configuración regional de Windows Media Player.                                                                                                                                     |
| *UserLocale* | IDENTIFICADOR de configuración regional de Windows. El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.        |
| *version*    | Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





