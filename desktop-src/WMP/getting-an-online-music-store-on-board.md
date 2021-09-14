---
title: Obtención de una Música store en línea
description: Obtención de una Música store en línea
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Reproductor de Windows Media Tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcff5aeed04ff2e60b03e7b546de23f1d0d747b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068433"
---
# <a name="getting-an-online-music-store-on-board"></a>Obtención de una Música store en línea

En este tema se describe el proceso de incorporar un almacén de medios digitales en línea para Reproductor de Windows Media. El tiempo necesario para el proceso de incorporación de principio a fin es aproximadamente de 45-60 DÍAS LABORABLES. Las dos fases del proceso de incorporación se describen en la tabla siguiente.




| Fase | Descripción | 
|-------|-------------|
| Pending | <ul><li>Envía a Microsoft la información de contacto necesaria, la información de inicio y las cuentas de validación.</li><li>Microsoft le envía una clave de prueba y una clave de producción.</li><li>Pruebe la tienda en línea con Reproductor de Windows Media.</li><li>Envíe contratos firmados a Microsoft.</li></ul> | 
| Validación | Microsoft valida la tienda en línea. | 




 

Después de completar las fases pendientes y de validación, Microsoft publicará su tienda en línea.

## <a name="pending-stage"></a>Fase pendiente

La fase pendiente le ofrece la oportunidad de probar la tienda en línea en Reproductor de Windows Media. También es un buen momento para asegurarse de que se firman todos los contratos y contratos necesarios. Para empezar, envíe a Microsoft la siguiente información, tal como se define más adelante en este tema:

-   Información de contacto
-   Información de inicio
-   Cuentas de validación

Tras recibir la información de contacto e inicio, Microsoft le enviará una clave de prueba y una clave de producción. Después de agregar la clave de prueba al registro y reiniciar el reproductor, la tienda en línea aparecerá en el reproductor y podrá probarla. Para obtener información sobre dónde colocar la clave de prueba en el Registro, vea Claves y entradas del Registro para un almacén en línea de tipo [1](registry-keys-and-entries-for-a-type-1-online-store.md) o Claves del Registro y entradas para un almacén en línea de tipo [2.](registry-keys-and-entries-for-a-type-2-online-store.md)

Debe probar todos los aspectos de la tienda en línea, incluida su interfaz de usuario y su complemento. Como parte del proceso de pruebas, debe ejecutar las pruebas descritas en Pruebas de validación para el tipo [2 Online Música Stores](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Los almacenes de tipo 1 deben superar todas las pruebas de validación para los almacenes de tipo 2, además de algunas pruebas adicionales que son específicas de la experiencia de tipo 1. Para obtener información sobre las pruebas de validación de tipo 1, póngase en contacto con Reproductor de Windows Media Services Virtual Team en mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Información de contacto

En la tabla siguiente se muestra la información de contacto que Microsoft requiere para su tienda en línea. Rellene el formulario [de información de contacto](contact-information-form-for-an-online-music-store.md) y envíelo al equipo virtual de Reproductor de Windows Media Services en mpsvctm@microsoft.com .



| Elemento                     | Descripción                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nombre de la tienda               | Nombre de marca de la tienda                                                            |
| Nombre del proveedor            | Nombre de la empresa de la etiqueta blanca o proveedor (si es diferente)                               |
| Configuración regional de la tienda             | Las Windows configuración regional del usuario que el almacén debe mostrar en                                |
| Categoría de la tienda           | Música, Radio, Película, TV, Deportes, Noticias, Audio Entretenimiento u Otros (describa) |
| Modelo de compra           | Compra, alquiler, suscripción u otros (describa)                            |
| Idioma de la tienda           |                                                                                           |
| Almacenar nombres de contacto    |                                                                                           |
| Correo electrónico de contacto de la tienda  |                                                                                           |
| Cuentas de MSFT Passport | Esto es para posibles nominaciones futuras en programas de desarrollo beta y de asociados.         |
| Dirección de envío         | Sin P.O. Cuadros                                                                             |
| City                     |                                                                                           |
| State                    |                                                                                           |
| Código postal              |                                                                                           |
| País/región           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contacto de encuesta           | ¿Está bien si nos comunicaremos con usted sobre su experiencia con el programa en el futuro?        |



 

## <a name="startup-information"></a>Información de inicio

Para cada región geográfica a la que prestará servicio la tienda, envíe a Microsoft un conjunto de información de inicio para el almacén de pruebas, un conjunto de información de inicio para el almacén de producción y un conjunto de cuentas de validación.

El tema [Formulario de información de inicio](startup-information-form-for-an-online-music-store.md) para un almacén de Música en línea contiene dos copias del formulario Información de inicio y una copia del formulario Cuentas de validación. Rellene los formularios y envíelos al equipo virtual de Reproductor de Windows Media Services en mpsvctm@microsoft.com .

En la tabla siguiente se describe la información de inicio que Microsoft requiere para su tienda en línea.



| Elemento                                                                                                     | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección URL XML de información de servicio (límite de 2048 caracteres)                                                              | Dirección URL en la Reproductor de Windows Media obtiene el [documento XML de ServiceInfo](serviceinfo-document.md).                                                                                                                                         |
| Clave de servicio (identificador único)                                                                                  | Cadena que identifica de forma única la tienda en línea. Debe crear uno para producción y otro para pruebas (por ejemplo, "MyStore" y "MyStoreTest"). Tenga en cuenta que una clave de servicio no es lo mismo que una clave de prueba.                        |
| Nombre descriptivo (límite de 30 caracteres)                                                                       | Nombre del almacén que se muestra en el selector Reproductor de Windows Media servicio.                                                                                                                                                        |
| Dirección URL de la imagen de menú (límite de 2048 caracteres)                                                                    | Dirección URL donde Reproductor de Windows Media el logotipo de 15 x 15 píxeles que se muestra en el selector de servicios.                                                                                                                                 |
| Comprar Música URL (límite de 2048 caracteres)<br/> (Solo tiendas de música integradas)<br/>                | La dirección URL que usan los vínculos "Comprar CD" y "Comprar cd" Música Online".                                                                                                                                                              |
| DIRECCIÓN URL de compra de IU de 10 pies (límite de 2048 caracteres)<br/> (Solo tiendas de música integradas: opcional)<br/> | Dirección URL que usan los vínculos "Comprar CD" y "Comprar Música Online" del reproductor en Windows XP Media Center Edition y en Windows Media Center en Windows Vista.                                                                              |
| Logotipo de la tienda (130w x 30h)<br/> (Adjunte el archivo PNG por separado).<br/>                              | Logotipo de la tienda que se muestra en la información sobre herramientas que aparece cuando el mouse está sobre la imagen de examinar todo. Este logotipo debe ser un archivo con formato PNG y preferiblemente con mezcla alfa para que pueda ajustarse a los cambios de color en Reproductor de Windows Media. |
| Imagen de exploración completa (108w x 108h)<br/> (Adjunte el archivo PNG por separado).<br/>                       | Breve descripción en la información sobre herramientas que aparece cuando el mouse está sobre la imagen de exploración.                                                                                                                                               |
| Texto de descripción del almacén (límite de 110 caracteres)                                                             | Texto que aparece en la información sobre herramientas debajo del texto de descripción del almacén.                                                                                                                                                                        |
| Texto para hipervínculo (límite de 45 caracteres)                                                                  | Logotipo de la tienda que se muestra en la página Examinar todas las tiendas en línea. Debe ser un archivo con formato PNG y preferiblemente con mezcla alfa para que pueda ajustarse a los cambios de color en Reproductor de Windows Media.                                           |



 

> [!Note]  
> La imagen browse-all de 108 x 108 píxeles es un requisito para Reproductor de Windows Media 11 y versiones posteriores.

 

> [!Note]  
> En Reproductor de Windows Media 11 y versiones posteriores, se omiten los elementos ServiceTask2 y ServiceTask3 del documento XML ServiceInfo. Para obtener información detallada sobre el documento XML de ServiceInfo, vea [ServiceInfo Document](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Cuentas de validación

Para completar el proceso de validación descrito en la sección Fase de validación siguiente, Microsoft requiere cinco (5) cuentas de validación para cada tipo de cuenta que ofrece la tienda en línea. Por ejemplo, si ofrece cuentas que diferencian entre características y funcionalidades, como básicas y premium, Microsoft necesitará cinco (5) cuentas de validación para cada tipo, para un total de diez (10) cuentas.

Envíe el nombre de usuario y la contraseña de cada cuenta de validación a mpsvctm@microsoft.com . Incluya también el nombre de una persona con la que Microsoft pueda ponerse en contacto con respecto a las cuentas de validación. Estas cuentas se usarán para la validación mensual en curso, por lo que debe incluir un proceso para "volver a cargar" las cuentas. Uno de los problemas más comunes se produce cuando una tienda en línea no proporciona crédito de compra suficiente para que Microsoft valide todos los escenarios de compra. Las cuentas deben permanecer activas una vez completado el proceso de incorporación.

## <a name="validation-stage"></a>Fase de validación

Durante la fase de validación, Microsoft comprueba que las características principales de la tienda en línea funcionan correctamente. Para todos los almacenes (tipo 1 y tipo 2), Microsoft ejecuta las pruebas de comprobación que se detallan en Pruebas de validación para el tipo [2 En](validation-tests-for-type-2-online-music-stores.md)línea Música Almacenes . Microsoft también ejecuta algunas pruebas de validación adicionales para almacenes de tipo 1. Si tiene alguna pregunta sobre la fase de validación de almacenes de tipo 1, envíe un correo electrónico a mpsvctm@microsoft.com .

Durante la fase de validación, Microsoft realiza dos pases de validación. El primer pase se aplica a Release Candidate 1 (RC1) de la tienda en línea. Si la tienda pasa la validación RC1, debe bloquearla y no realizar más cambios. Microsoft realizará un segundo paso de validación en la tienda incluso si la tienda supera la validación RC1.

Si la tienda produce un error en cualquier parte del paso de validación RC1, tendrá dos semanas para crear una segunda versión candidata para lanzamiento (RC2), que Microsoft validará durante el paso de validación rc2.

Si el almacén produce un error en cualquier parte de la validación rc2, debe esperar hasta el siguiente inicio.

## <a name="test-and-production-keys"></a>Claves de prueba y producción

Recuerde que, durante la fase pendiente, envió a Microsoft dos conjuntos de información de inicio: uno para el almacén de pruebas y otro para el almacén de producción. Recuerde también que Microsoft le envió dos claves: una clave de prueba y una clave de producción.

La clave de prueba es completamente para su propio uso. Cuando la clave de prueba está en el Registro, Reproductor de Windows Media la dirección URL de ServiceInfo que envió para el almacén de pruebas.

Cuando la clave de producción está en el registro, Reproductor de Windows Media la dirección URL de ServiceInfo que envió para el almacén de producción. Microsoft usa la clave de producción durante la fase de validación. Microsoft nunca usa la clave de prueba para la validación.

Cuando la tienda esté en directo, Reproductor de Windows Media la dirección URL de ServiceInfo que envió para el almacén de producción.

Como regla general, el almacén de pruebas debe ser el lugar donde desarrolle el servicio y realice cambios diarios. El almacén de producción debe ser el lugar donde mantenga una versión estable del servicio.

## <a name="common-on-boarding-problems"></a>Problemas comunes de incorporación

Estos son algunos problemas comunes que pueden hacer que el almacén no pueda realizar pruebas de validación.

-   Error al pasar de servidores de prueba a servidores de producción. Esto provoca muchos problemas, como páginas que faltan, configuración de seguridad y IIS no válida, y cuentas de prueba que ya no funcionan.
-   El vínculo Comprar (o Vínculo a la tienda) del área Reproducción ahora no es válido. Esto puede hacer que la tienda no valide aunque todo lo demás funcione.
-   El equipo de validación de Microsoft probará varios escenarios de compra que van desde compras pequeñas hasta compras muy grandes. Debe proporcionar una manera fácil de actuar como consumidor dentro de su tienda. No se puede validar la tienda si el equipo de validación no tiene suficientes créditos de compra para validar todos estos escenarios.

Para obtener una lista más completa de los problemas comunes de incorporación y las preguntas más frecuentes compiladas por el equipo virtual de Reproductor de Windows Media Services, consulte [Common On-Boarding Problems for Online Música Stores](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Kit de bienvenida de tiendas en línea](online-stores-welcome-kit.md)
</dt> </dl>

 

 





