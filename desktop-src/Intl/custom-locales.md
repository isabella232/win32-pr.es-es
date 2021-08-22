---
description: Configuraciones regionales personalizadas
ms.assetid: 110efeab-c02f-4244-8950-a975cfc91e8a
title: Configuraciones regionales personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda75d0d097bf6860e1385bb2557d56c2b2d2a1df530404781817590e381b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754925"
---
# <a name="custom-locales"></a>Configuraciones regionales personalizadas

**Windows Vista y versiones posteriores:** Las configuraciones regionales personalizadas admiten propiedades internacionales que proporcionan una experiencia de usuario más adecuada culturalmente que las que se suministran con las configuraciones regionales estándar enviadas por Microsoft con el sistema operativo. El uso de configuraciones regionales personalizadas permite a los administradores ampliar el conjunto de configuraciones regionales proporcionado por Microsoft o reemplazar los datos de una configuración regional que se distribuye por Windows, por ejemplo, símbolos de moneda o nombres de los meses del año.

Los dos tipos de configuraciones regionales personalizadas son configuraciones regionales complementarias y configuraciones regionales de reemplazo. Las configuraciones regionales complementarias son configuraciones regionales personalizadas que permiten a las empresas, universidades, gobiernos y otros terceros crear datos de configuración regional que no están disponibles en el sistema operativo de envío. Las configuraciones regionales de reemplazo son configuraciones regionales [personalizadas](locale-identifiers.md) que se envían con el sistema operativo sin cambiar los identificadores de configuración regional ni los [nombres de configuración regional.](locale-names.md)

Puede usar la utilidad Generador de configuración regional proporcionada por NLS para compilar configuraciones regionales personalizadas. Para obtener más información, vea [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158). Las instrucciones para usar configuraciones regionales personalizadas en las aplicaciones se [proporcionan en Trabajar con configuraciones regionales personalizadas.](working-with-custom-locales.md)

## <a name="comparison-of-custom-locale-types"></a>Comparación de tipos de configuración regional personalizados

En la tabla siguiente se describen las diferencias entre las configuraciones regionales complementarias y de reemplazo.



| Elemento                                                                                                                           | Configuración regional complementaria                                                                                                                                                                                                                   | Configuración regional de reemplazo                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Calendarios                                                                                                                      | Puede incluir cualquiera de los calendarios proporcionados por Microsoft. Al menos uno de los calendarios proporcionados debe ser el calendario gregoriano localizado.                                                                                              | Puede incluir cualquiera de los calendarios proporcionados por Microsoft. Al menos uno de los calendarios proporcionados debe ser el calendario gregoriano localizado y la colección debe incluir el calendario predeterminado de la configuración regional reemplazada. |
| Ordenación                                                                                                                        | Puede usar cualquiera de las ordenaciones proporcionadas por Microsoft.                                                                                                                                                                                          | Conserva el comportamiento de ordenación de la configuración regional que se va a reemplazar.                                                                                                                                                            |
| Nombres de día y mes                                                                                                            | Solo se puede personalizar para el calendario gregoriano estándar, no para calendarios no gregorianos y no para calendarios gregorianos especializados, como el calendario gregoriano de Oriente Medio francés.                                           | Igual que para la configuración regional complementaria.                                                                                                                                                                                      |
| Nombre de idioma ([LOCALE \_ SLANGUAGE](locale-slanguage.md) o [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)) | Devuelve [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) o [LOCALE \_ SNATIVELANGUAGENAME](locale-snative-constants.md).                                                                                                       | Mantiene el nombre de idioma de la configuración regional que se va a reemplazar.                                                                                                                                                                 |
| Identificador de configuración regional                                                                                                              | Establezca en [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md) a menos que la configuración regional sea la configuración regional de Estándares y formatos seleccionada actualmente por el usuario, en cuyo caso se establece en [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md). | Mantiene el identificador de configuración regional de la configuración regional que se va a reemplazar.                                                                                                                                                             |
| Nombre de la configuración regional                                                                                                                    | Arbitrario; debe ajustarse al patrón que se describe en [Nombres de configuración regional](locale-names.md).                                                                                                                                                      | Mantiene el nombre de configuración regional de la configuración regional que se va a reemplazar.                                                                                                                                                                   |



 

## <a name="supplemental-locale-examples"></a>Ejemplos complementarios de configuración regional



| Nombre de la configuración regional    | Descripción                                                                                                                                                                                                                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-CA-fabricam | Fabricam es un fabricante canadiense de equipos con oficinas en todo el mundo. Para proporcionar un comportamiento coherente de la interfaz de usuario para todos sus equipos, la empresa desarrolla una configuración regional para usar en toda la empresa.                                                                                                                                                          |
| fr-US          | Woodlawn Bank usa Windows XP Embedded para sus equipos de teller automatizados (ATMs), que el banco distribuye a través de Norteamérica con interfaces de usuario en francés, inglés y español. Para proporcionar una experiencia coherente, el banco crea una configuración regional para francés en la Estados Unidos que tiene formatos de Estados Unidos, pero nombres de día y mes en francés. |



 

## <a name="replacement-locale-example"></a>Ejemplo de configuración regional de reemplazo



| Nombre de la configuración regional | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| en-US       | Fabricam es un fabricante canadiense de equipos con oficinas en todo el mundo. Para proporcionar un comportamiento coherente de la interfaz de usuario para todos sus equipos, la empresa desarrolla una configuración regional para usar en toda la empresa. Usa un reloj de 24 horas, pero de lo contrario se comporta como la configuración regional de inglés compatible (Estados Unidos). Dado que la configuración regional personalizada es tan similar a la configuración regional admitida, Fabricam decide implementarla como configuración regional de reemplazo en lugar de como configuración regional complementaria. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Trabajar con configuraciones regionales personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



