---
description: Puede tener acceso a todas las fechas y horas de Modelo de información común (CIM) en WMI utilizando uno de los dos formatos de longitud fija específicos de WMI y CIM. En la secuencia de comandos, use el objeto SWbemDateTime para convertirlos en fechas y horas normales.
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716765"
---
# <a name="cim_datetime"></a>\_fecha y hora de CIM

Puede tener acceso a todas las fechas y horas de [*modelo de información común (CIM)*](gloss-c.md) en WMI utilizando uno de los dos formatos de longitud fija específicos de WMI y CIM. En la secuencia de comandos, use el objeto [**SWbemDateTime**](swbemdatetime.md) para convertirlos en fechas y horas normales.

En las secciones siguientes se describe cómo usar los formatos de fecha y hora de WMI.

## <a name="format"></a>Formato

En la tabla siguiente se enumeran los dos formatos de fecha y hora usados por WMI.



| Formato                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DATETIME](datetime.md)<br/> *aaaammddhhmmss. mmmmmmsUUU*<br/>                             | Formato en el que se almacenan los valores [**DateTime**](datetime.md) de CIM. Este formato es independiente de la configuración regional, por lo que puede escribir un script que se ejecute en cualquier equipo. Debe usar este formato para definir una fecha y hora en [*Managed Object Format (MOF)*](gloss-m.md), o al escribir en una instancia de mediante la [API com para WMI](com-api-for-wmi.md) o la [API de scripting para WMI](scripting-api-for-wmi.md). Para obtener más información, vea [modificar una propiedad de instancia](modifying-an-instance-property.md). |
| Formato válido solo en consultas de lenguaje de consulta de WMI (WQL).<br/> *aaaa-mm-dd HH: MM: SS: MMM*<br/> | Este formato se puede usar en scripts que usan los métodos [**SWbemDateTime**](swbemdatetime.md) . Para obtener más información, vea [consultar WMI](querying-wmi.md) o [consultar con WQL](querying-with-wql.md). Este formato no es independiente de la configuración regional. El orden de año, mes y día depende de la configuración de formato de idioma y configuración regional de la sesión de usuario. Por ejemplo, mientras que el valor predeterminado para Estados Unidos inglés es "mm-dd-aaaa HH: mm: SS: MMM", el formato de la mayoría de los demás países o regiones es "AAAA-MM-DD HH: mm: SS: MMM".       |



 

En la tabla siguiente se enumeran los campos de los formatos.



| Campo    | Descripción                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *yyyy*   | Año de cuatro dígitos (0000 a 9999). La implementación de puede restringir el intervalo admitido. Por ejemplo, una implementación de solo puede admitir los años 1980 a 2099.                                                                         |
| *mm*     | Mes de dos dígitos (del 01 al 12).                                                                                                                                                                                                                |
| *dd*     | Día del mes de dos dígitos (del 01 al 31). Este valor debe ser adecuado para el mes. Por ejemplo, el 31 de febrero no es válido. Sin embargo, la implementación no tiene que comprobar si hay datos válidos.                                            |
| *HH*     | Hora de dos dígitos del día con el reloj de 24 horas (de 00 a 23).                                                                                                                                                                              |
| *MM*     | Minuto de dos dígitos en la hora (de 00 a 59).                                                                                                                                                                                                   |
| *SS*     | Número de segundos de dos dígitos en el minuto (de 00 a 59).                                                                                                                                                                                      |
| *MMMMMM* | Número de seis dígitos de microsegundos en el segundo (000000 a 999999). La implementación no tiene que admitir la evaluación mediante este campo. Sin embargo, este campo siempre debe estar presente para conservar la naturaleza de longitud fija de la cadena. |
| *mmm*    | Número de milisegundos de tres dígitos en el minuto (de 000 a 999).                                                                                                                                                                             |
| *s*      | Signo más (+) o signo menos (-) para indicar un desplazamiento positivo o negativo respecto a las horas universales coordinadas (UTC).                                                                                                                               |
| *UUU*    | Desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC. Para WMI, se recomienda, aunque no es necesario, convertir las horas a GMT (un desplazamiento de UTC de cero).                                              |



 

Debe escribir todos los campos con la longitud indicada, utilizando los ceros iniciales según corresponda para el tipo. Sin embargo, utilice asteriscos para indicar los campos no usados o como un valor comodín. Puede usar un asterisco ( \* ) en cualquier lugar excepto la cláusula **Where** de una consulta. Por ejemplo, una fecha y hora con un año no especificado pueden producirse en cualquier año. Si desea dejar un campo sin especificar, debe reemplazar el campo completo por asteriscos.

En los siguientes ejemplos se describen los usos válidos y no válidos de asteriscos:

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (legal)
-   1998-04-16 \* \* \* \* \* \* : \* \* \* (no válido)
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (no válido)
-   199 \* -04-16 \* \* \* \* \* \* : \* \* \* (no válido)

Si se usa un valor de fecha y hora para representar un punto concreto en el tiempo, todos sus campos deben incluir datos. Si se usa para representar un intervalo de tiempo, solo los campos necesarios para transmitir la duración deben incluir datos.

En el ejemplo siguiente se describe "primero de abril": una fecha relativa a un año no especificado, pero sigue siendo un punto definido si el nivel de detalle de la medida es un día.

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* : \* \* \* (no válido)

## <a name="setting-utc-offset-and-gmt"></a>Establecer el desplazamiento de UTC y GMT

En los ejemplos siguientes se describe cómo se puede definir una hora sin zona horaria colocando asteriscos en el campo UUU después del signo más o menos:

-   19980401135809.000000 +\*\*\*
-   19980401135809,000000:\*\*\*
-   1998-04-01 13:58:09: \* \* \* (no válido)

Una aplicación interpreta una referencia de fecha y hora sin zona en un CHRONOMETER de datos abstracto local en el sistema operativo que se ejecuta. Por ejemplo, los equipos portátiles pueden tener relojes internos cuya configuración puede corresponder a la zona horaria geográfica. Puede interpretar el tiempo sin zona sustituyendo la zona horaria del origen de hora abstracto actual en lugar de la zona horaria local.

Debe tener en cuenta especial el significado del desplazamiento UTC con fechas y horas en las consultas. En general, las comparaciones de equivalencia, mayor que o menor que funcionan entre dos fechas y horas si las fechas y las horas usan el mismo desplazamiento de UTC. Cuando se trabaja con fechas y horas que se producen con distintos desplazamientos de zona horaria, primero debe convertir las fechas y horas a GMT.

Las consultas que implican fechas y horas relativas con asteriscos en uno o más subcampos solo son significativas para WMI cuando se comparan con la equivalencia. Además, WMI no permite el uso de asteriscos como caracteres comodín. En su lugar, WMI compara fechas y horas relativas en función de caracteres.

En los siguientes ejemplos se describen dos fechas en las que una consulta WMI no tiene el mismo valor:

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>Convertir a formato de fecha de FILETIME o VT \_

El formato de [**fecha y hora**](datetime.md) de CIM solo se utiliza en WMI. Puede convertir a y desde el formato WMI y el formato de fecha FILETIME o VT llamando a \_ los métodos del objeto de scripting [**SWbemDateTime**](swbemdatetime.md) . Una estructura de **fecha y hora** de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) es un valor de 64 bits que usan los sistemas operativos Windows de 32 bits. El \_ formato de fecha VT es un valor DateTime de la variante de automatización utilizado por Visual Basic y ActiveX. En la tabla siguiente se enumeran los métodos de conversión.



| Método                                                         | Descripción                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md) | Obtiene un valor [**DateTime**](datetime.md) en formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .                |
| [**SWbemDateTime. Getvardate (**](swbemdatetime-getvardate.md)   | Obtiene un valor [**DateTime**](datetime.md) en \_ formato de fecha VT.                                         |
| [**SWbemDateTime.SetFileTime**](swbemdatetime-setvardate.md)  | Establece una propiedad [**DateTime**](datetime.md) usando una fecha de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como entrada. |
| [**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)   | Establece una propiedad [**DateTime**](datetime.md) usando una \_ fecha de datos de VT como entrada.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de fecha y hora](date-and-time-format.md)
</dt> <dt>

[Acerca de WMI](about-wmi.md)
</dt> <dt>

[Tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md)
</dt> <dt>

[Formato de intervalo](interval-format.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServicesEx. put**](swbemservicesex-put.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

