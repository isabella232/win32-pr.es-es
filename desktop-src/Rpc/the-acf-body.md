---
title: El cuerpo ACF
description: El cuerpo ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078517"
---
# <a name="the-acf-body"></a>El cuerpo ACF

El cuerpo ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL. El cuerpo de ACF puede estar vacío o puede contener atributos de [**inclusión**](/windows/desktop/Midl/include)ACF, [**typedef**](/windows/desktop/Midl/typedef), función y parámetro. Todos estos elementos son opcionales. Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF reemplazan a los atributos del encabezado ACF.

ACF especifica el comportamiento en el equipo local y no afecta a los datos transmitidos a través de la red. Se utiliza para especificar los detalles de un código auxiliar que se va a generar. En el modo de compatibilidad de DCE ([**/OSF**](/windows/desktop/Midl/-osf)), el ACF no afecta a la interacción entre códigos auxiliares, sino entre el código auxiliar y el código de aplicación.

Un parámetro especificado en ACF debe ser uno de los parámetros especificados en el archivo IDL. El orden de especificación del parámetro en ACF no es significativo porque la coincidencia es por nombre, no por posición. La lista de parámetros de ACF puede estar vacía, incluso si la lista de parámetros de la signatura IDL correspondiente no es (pero no se recomienda). Los declaradores abstractos (parámetros sin nombre) en el archivo IDL hacen que el compilador de MIDL informe de los errores al procesar el ACF porque no se encuentra el parámetro.

La Directiva de **inclusión** ACF especifica los archivos de encabezado que aparecen en el encabezado generado como parte de una instrucción **\# include** estándar de C-preprocesador. La palabra clave ACF **incluye** diferencias entre una directiva **\# include** . La palabra clave ACF **incluye** que la línea "**\# include** *filename*" aparezca en el archivo de encabezado generado, mientras que la Directiva del lenguaje C "**\# include** *filename*" hace que el contenido de ese archivo se coloque en el ACF.

La instrucción [**typedef**](/windows/desktop/Midl/typedef) de ACF permite aplicar atributos de tipo ACF a los tipos definidos anteriormente en el archivo IDL. La sintaxis de **typedef** de ACF difiere de la sintaxis de **typedef** de C.

Los atributos de función ACF permiten especificar los atributos que se aplican a la función en conjunto. Para obtener más información, vea **\[** [**código**](/windows/desktop/Midl/code) **\]** , **\[** [**optimizar**](/windows/desktop/Midl/optimize) **\]** y **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .

Los atributos del parámetro ACF permiten especificar los atributos que se aplican a los parámetros individuales de la función. Para obtener más información, vea **\[** [**\_ recuento de bytes**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**configuración de/APP \_**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[\_identificador automático\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[codifica\]**](../midl/code.md)
</dt> <dt>

[**\[\_identificador explícito\]**](../midl/explicit-handle.md)
</dt> <dt>

[El archivo de lenguaje de definición de interfaz (IDL)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[\_identificador implícito\]**](../midl/implicit-handle.md)
</dt> <dt>

[**inclui**](/windows/desktop/Midl/include)
</dt> <dt>

[MIDL](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[optimiz\]**](../midl/optimize.md)
</dt> <dt>

[**\[representar \_ como\]**](../midl/represent-as.md)
</dt> <dt>

[**typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 