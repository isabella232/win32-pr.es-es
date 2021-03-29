---
title: Obtención de una tienda de música en línea en el panel
description: Obtención de una tienda de música en línea en el panel
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c5d13e14e95e88e83d42fd7d5cd00551bb507
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994437"
---
# <a name="getting-an-online-music-store-on-board"></a>Obtención de una tienda de música en línea en el panel

En este tema se describe el proceso de incorporación de un almacén de medios digitales en línea en el panel de Media Player de Windows. El tiempo necesario para que el proceso de incorporación de principio a fin sea de aproximadamente 45-60 días LABORAbles. En la tabla siguiente se describen las dos fases del proceso de incorporación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fase</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pending</td>
<td><ul>
<li>Envía a Microsoft la información de contacto necesaria, la información de inicio y las cuentas de validación.</li>
<li>Microsoft le envía una clave de prueba y una clave de producción.</li>
<li>Probará la tienda en línea con Windows Media Player.</li>
<li>Envía acuerdos y contratos firmados a Microsoft.</li>
</ul></td>
</tr>
<tr class="even">
<td>Validación</td>
<td>Microsoft valida la tienda en línea.</td>
</tr>
</tbody>
</table>



 

Después de completar las fases de validación pendientes y, Microsoft publicará la tienda en línea.

## <a name="pending-stage"></a>Fase pendiente

La fase pendiente le ofrece la oportunidad de probar la tienda en línea en Windows Media Player. También es un buen momento para asegurarse de que todos los contratos y contratos necesarios están firmados. Para empezar, envíe a Microsoft la siguiente información, tal y como se define más adelante en este tema:

-   Información de contacto
-   Información de inicio
-   Cuentas de validación

Tras recibir la información de contacto y de inicio, Microsoft le enviará una clave de prueba y una clave de producción. Una vez que haya agregado la clave de prueba al registro y haya reiniciado el reproductor, la tienda en línea aparecerá en el reproductor y podrá probarla. Para obtener información acerca de dónde colocar la clave de prueba en el registro, consulte [las entradas y claves del registro de una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md) o [las entradas y claves del registro para un almacén en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

Debe probar todos los aspectos de la tienda en línea, incluida su interfaz de usuario y su complemento. Como parte del proceso de pruebas, debe ejecutar las pruebas descritas en [pruebas de validación para las tiendas de música en línea de tipo 2](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Los almacenes de tipo 1 deben superar todas las pruebas de validación para los almacenes de tipo 2 y algunas pruebas adicionales específicas de la experiencia de tipo 1. Para obtener información acerca de las pruebas de validación de tipo 1, póngase en contacto con el equipo virtual de Windows Media Player Services en mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Información de contacto

En la tabla siguiente se muestra la información de contacto que Microsoft requiere para la tienda en línea. Rellene el [formulario de información de contacto](contact-information-form-for-an-online-music-store.md) y envíelo al equipo virtual de Windows Media Player Services en mpsvctm@microsoft.com .



| Elemento                     | Descripción                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nombre de la tienda               | El nombre con marca de la tienda                                                            |
| Nombre del proveedor            | El nombre de la compañía del proveedor o la etiqueta blanca (si es diferente)                               |
| Configuración regional de la tienda             | La configuración regional del usuario de Windows del almacén debe mostrarse en                                |
| Categoría de la tienda           | Música, radio, película, TV, deportes, noticias, entretenimiento de audio y otros (describir) |
| Modelo de compra           | Compra, alquiler, suscripción y/u otros (describe)                            |
| Idioma del almacén           |                                                                                           |
| Almacenar los nombres de contacto    |                                                                                           |
| Almacenar correo electrónico de contacto  |                                                                                           |
| Cuentas de MSFT Passport | Esto es para posibles supuestos futuros en programas de desarrollo de asociados y beta.         |
| Dirección de envío         | Sin correos Cuadros                                                                             |
| City (Ciudad)                     |                                                                                           |
| Estado                    |                                                                                           |
| Código postal              |                                                                                           |
| País/región           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contacto de encuestas           | ¿Es correcto si nos pondremos en contacto con usted acerca de su experiencia con el programa en el futuro?        |



 

## <a name="startup-information"></a>Información de inicio

Para cada región geográfica a la que sirva su tienda, envíe a Microsoft un conjunto de información de inicio para el almacén de pruebas, un conjunto de información de inicio para el almacén de producción y un conjunto de cuentas de validación.

El [formulario información de inicio de un tema de una tienda de música en línea](startup-information-form-for-an-online-music-store.md) contiene dos copias del formulario información de inicio y una copia del formulario cuentas de validación. Rellene los formularios y envíelos al equipo virtual de Windows Media Player Services en mpsvctm@microsoft.com .

En la tabla siguiente se describe la información de inicio que Microsoft necesita para la tienda en línea.



| Elemento                                                                                                     | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección URL XML de información de servicio (límite de 2048 caracteres)                                                              | La dirección URL donde Windows Media Player obtiene el [documento XML ServiceInfo](serviceinfo-document.md).                                                                                                                                         |
| Clave de servicio (identificador único)                                                                                  | Cadena que identifica de forma única la tienda en línea. Debe crear una para producción y otra para las pruebas (por ejemplo, "My" y "MyStoreTest"). Tenga en cuenta que una clave de servicio no es lo mismo que una clave de prueba.                        |
| Nombre descriptivo (límite de 30 caracteres)                                                                       | El nombre del almacén que se muestra en el selector de servicio de Windows Media Player.                                                                                                                                                        |
| URL de imagen de menú (límite de 2048 caracteres)                                                                    | La dirección URL donde Windows Media Player recupera el logotipo de 15 x 15 píxeles que muestra en el selector de servicio.                                                                                                                                 |
| Comprar dirección URL de música (límite de 2048 caracteres)<br/> (Solo tiendas de música integradas)<br/>                | La dirección URL que usan los vínculos "comprar CD" y "comprar música en línea" del reproductor.                                                                                                                                                              |
| Dirección URL de compra de la interfaz de usuario de 10 ft (límite de 2048 caracteres)<br/> (Solo almacenes de música integrados: opcional)<br/> | La dirección URL que usan los vínculos "comprar CD" y "comprar música en línea" del reproductor en Windows XP Media Center Edition y en Windows Media Center en Windows Vista.                                                                              |
| Logotipo de la tienda (130W x 30 h)<br/> (Adjunte el archivo PNG por separado).<br/>                              | El logotipo de la tienda que se muestra en la información sobre herramientas que aparece cuando el mouse está encima de la imagen de examinar todo. Este logotipo debe ser un archivo con formato PNG y preferentemente mezclado alfa para que pueda ajustarse a los cambios de color en Windows Media Player. |
| Examinar: toda la imagen (108W x 108h)<br/> (Adjunte el archivo PNG por separado).<br/>                       | Breve descripción de la información sobre herramientas que aparece cuando el mouse está sobre la imagen de exploración.                                                                                                                                               |
| Texto de descripción de la tienda (límite de 110 caracteres)                                                             | Texto que aparece en la información sobre herramientas debajo del texto de descripción de la tienda.                                                                                                                                                                        |
| Texto del hipervínculo (límite de 45 caracteres)                                                                  | El logotipo de la tienda que se muestra en la página examinar todas las tiendas en línea. Debe ser un archivo con formato PNG y preferentemente mezclado alfa para que pueda ajustarse a los cambios de color en Windows Media Player.                                           |



 

> [!Note]  
> La imagen Browse-All de 108 x 108 píxeles es un requisito para Windows Media Player 11 y versiones posteriores.

 

> [!Note]  
> En Windows Media Player 11 y versiones posteriores, se omiten los elementos ServiceTask2 y ServiceTask3 del documento XML ServiceInfo. Para obtener información detallada sobre el documento XML ServiceInfo, vea el [documento serviceinfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Cuentas de validación

Para completar el proceso de validación que se describe en la sección fase de validación que aparece a continuación, Microsoft requiere cinco (5) cuentas de validación para cada tipo de cuenta que ofrece la tienda en línea. Por ejemplo, si ofrece cuentas que diferencian entre las características y la funcionalidad, como Basic y Premium, Microsoft necesitará cinco (5) cuentas de validación para cada tipo, para un total de diez (10) cuentas.

Envíe el nombre de usuario y la contraseña de cada cuenta de validación a mpsvctm@microsoft.com . Incluya también el nombre de una persona a la que Microsoft pueda contactar con respecto a las cuentas de validación. Estas cuentas se usarán para la validación mensual continua, por lo que debe incluir un proceso para "recargar" las cuentas. Uno de los problemas más comunes se produce cuando una tienda en línea no proporciona un crédito de compra suficiente para que Microsoft valide todos los escenarios de compra. Las cuentas deben permanecer activas una vez completado el proceso de incorporación.

## <a name="validation-stage"></a>Fase de validación

Durante la fase de validación, Microsoft comprueba que las características principales de la tienda en línea funcionan correctamente. En todos los almacenes (tipo 1 y tipo 2), Microsoft ejecuta las pruebas de comprobación que se detallan en las [pruebas de validación de las tiendas de música en línea de tipo 2](validation-tests-for-type-2-online-music-stores.md). Microsoft también ejecuta algunas pruebas de validación adicionales para los almacenes de tipo 1. Si tiene alguna pregunta sobre la fase de validación de los almacenes de tipo 1, envíe un correo a mpsvctm@microsoft.com .

Durante la fase de validación, Microsoft realiza dos fases de validación. El primer paso se aplica a Release Candidate 1 (RC1) de la tienda en línea. Si el almacén pasa la validación RC1, debe bloquearla y no realizar ningún cambio más. Microsoft realizará un segundo paso de validación en la tienda, incluso si el almacén pasa la validación RC1.

Si el almacén produce un error en cualquier parte de la fase de validación de RC1, tendrá dos semanas para crear un segundo candidato de versión comercial (RC2), que Microsoft validará durante la fase de validación de RC2.

Si el almacén produce un error en cualquier parte de la validación de RC2, debe esperar hasta el siguiente inicio.

## <a name="test-and-production-keys"></a>Claves de prueba y de producción

Recuerde que, durante la fase pendiente, envió Microsoft dos conjuntos de información de Inicio: uno para el almacén de pruebas y otro para la tienda de producción. Recuerde también que Microsoft le ha enviado dos claves: una clave de prueba y una clave de producción.

La clave de prueba es totalmente para su propio uso. Cuando la clave de prueba está en el registro, Windows Media Player usa la dirección URL ServiceInfo que envió para el almacén de pruebas.

Cuando la clave de producción se encuentra en el registro, Windows Media Player usa la dirección URL de ServiceInfo que envió para la tienda de producción. Microsoft usa su clave de producción durante la fase de validación. Microsoft nunca usa su clave de prueba para la validación.

Cuando el almacén está activo, Windows Media Player usa la dirección URL de ServiceInfo que envió para la tienda de producción.

Como norma general, el almacén de pruebas debe ser el lugar en el que desarrolla el servicio y realiza cambios diarios. La tienda de producción debe ser el lugar donde se mantiene una versión estable del servicio.

## <a name="common-on-boarding-problems"></a>Problemas comunes de incorporación

Estos son algunos problemas comunes que pueden hacer que el almacén no supere las pruebas de validación.

-   No se pudo realizar la transición de los servidores de prueba a los servidores de producción. Esto conduce a muchos problemas, como las páginas que faltan, la configuración de seguridad y IIS no válida y las cuentas de prueba que ya no funcionan.
-   El vínculo comprar (o el vínculo de la tienda) del área reproducción en curso no es válido. Esto puede hacer que el almacén no supere la validación incluso cuando todo lo demás funciona.
-   El equipo de validación de Microsoft probará varios escenarios de compra que van desde pequeñas compras hasta compras de gran tamaño. Debe proporcionar una manera recargable para que actúen como un consumidor dentro de la tienda. No se puede validar la tienda si el equipo de validación no tiene suficientes créditos de compra para validar todos estos escenarios.

Para obtener una lista completa de los problemas comunes de incorporación y las preguntas más frecuentes compiladas por el equipo virtual de servicios de Windows Media Player, consulte [la sección sobre problemas comunes de incorporación para tiendas de música en línea](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Kit de bienvenida de tiendas en línea](online-stores-welcome-kit.md)
</dt> </dl>

 

 





