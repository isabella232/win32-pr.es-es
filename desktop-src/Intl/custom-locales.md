---
description: Configuraciones regionales personalizadas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Configuraciones regionales personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50108750fb1209aa210b04d8be9adcd48e5fd308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002784"
---
# <a name="custom-locales"></a>Configuraciones regionales personalizadas

**Windows Vista y versiones posteriores:** Las configuraciones regionales personalizadas admiten propiedades internacionales, lo que proporciona una experiencia de usuario más adecuada para la cultura que las que se proporcionan con las configuraciones regionales estándar enviadas por Microsoft con el sistema operativo. El uso de configuraciones regionales personalizadas permite a los administradores ampliar el conjunto de configuraciones regionales proporcionado por Microsoft o reemplazar los datos en una configuración regional que se distribuye con Windows, por ejemplo, los símbolos de moneda o los nombres de los meses del año.

Los dos tipos de configuraciones regionales personalizadas son configuraciones regionales complementarias y configuraciones regionales de reemplazo. Las configuraciones regionales complementarias son configuraciones regionales personalizadas que permiten a las empresas, universidades, gobiernos y terceros crear datos de configuración regional no disponibles en el sistema operativo de envío. Las configuraciones regionales de reemplazo son configuraciones regionales personalizadas que se incluyen con el sistema operativo sin cambiar los [identificadores de configuración regional](locale-identifiers.md) ni [los nombres de configuración regional](locale-names.md).

Puede usar la utilidad de configuración regional que proporciona NLS para compilar configuraciones regionales personalizadas. Para obtener más información, vea [generador de configuración regional de Microsoft](https://www.microsoft.com/download/details.aspx?id=41158). Las instrucciones para usar configuraciones regionales personalizadas en las aplicaciones se proporcionan al [trabajar con configuraciones regionales personalizadas](working-with-custom-locales.md).

## <a name="comparison-of-custom-locale-types"></a>Comparación de tipos de configuración regional personalizada

En la tabla siguiente se describen las diferencias entre las configuraciones regionales adicionales y de reemplazo.



| Elemento                                                                                                                           | Configuración regional complementaria                                                                                                                                                                                                                   | Configuración regional de reemplazo                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendarios                                                                                                                      | Puede incluir cualquiera de los calendarios proporcionados por Microsoft. Al menos uno de los calendarios proporcionados debe ser el calendario adaptado gregoriano.                                                                                              | Puede incluir cualquiera de los calendarios proporcionados por Microsoft. Al menos uno de los calendarios proporcionados debe ser el calendario adaptado gregoriano y la colección debe incluir el calendario predeterminado de la configuración regional reemplazada. |
| Ordenación                                                                                                                        | Puede utilizar cualquiera de las ordenaciones proporcionadas por Microsoft.                                                                                                                                                                                          | Conserva el comportamiento de ordenación de la configuración regional que se va a reemplazar.                                                                                                                                                            |
| Nombres de día y mes                                                                                                            | Solo se puede personalizar para el calendario gregoriano estándar, no para los calendarios no gregorianos y no para los Calendarios gregorianos especializados, como el calendario gregoriano intermedio de Oriente Medio.                                           | Igual que para la configuración regional complementaria.                                                                                                                                                                                      |
| Nombre de idioma ([configuración regional \_ SLANGUAGE](locale-slanguage.md) o [configuración regional \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Devuelve la [configuración regional \_ SNATIVELANGNAME](locale-snative-constants.md) o [locale \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantiene el nombre de idioma de la configuración regional que se va a reemplazar.                                                                                                                                                                 |
| Identificador de configuración regional                                                                                                              | Establezca en [configuración regional \_ personalizada \_ sin especificar](locale-custom-constants.md) , a menos que la configuración regional sea la configuración regional del usuario seleccionada actualmente y formatos, en cuyo caso se establece en [configuración \_ regional \_ predeterminada personalizada](locale-custom-constants.md). | Mantiene el identificador de configuración regional de la configuración regional que se va a reemplazar.                                                                                                                                                             |
| Nombre de configuración regional                                                                                                                    | Ejecutar debe ajustarse al patrón descrito en [nombres de configuración regional](locale-names.md).                                                                                                                                                      | Mantiene el nombre de la configuración regional de la configuración regional que se va a reemplazar.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Ejemplos de configuración regional complementaria



| Nombre de configuración regional    | Descripción                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam es un fabricante de PC canadienses con oficinas en todo el mundo. Para proporcionar un comportamiento coherente con la interfaz de usuario para todos sus equipos, la empresa desarrolla una configuración regional para usar toda la empresa.                                                                                                                                                          |
| fr-EE. UU.          | Woodlawn Bank usa Windows XP Embedded para sus cajeros automáticos, que el Banco envía a través de Norteamérica con las interfaces de usuario en francés, Inglés y español. Para proporcionar una experiencia coherente, el Banco crea una configuración regional para francés en el Estados Unidos que tiene formatos de Estados Unidos pero nombres de día y mes en francés. |



 

## <a name="replacement-locale-example"></a>Ejemplo de configuración regional de reemplazo



| Nombre de configuración regional | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| es-ES       | Fabricam es un fabricante de PC canadienses con oficinas en todo el mundo. Para proporcionar un comportamiento coherente con la interfaz de usuario para todos sus equipos, la empresa desarrolla una configuración regional para usar toda la empresa. Usa un reloj de 24 horas, pero de lo contrario se comporta como la configuración regional de inglés (Estados Unidos) admitida. Dado que la configuración regional personalizada es tan similar a la configuración regional admitida, Fabricam decide implementarla como una configuración regional de reemplazo en lugar de una configuración regional complementaria. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Trabajar con configuraciones regionales personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



