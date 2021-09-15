---
title: El cuerpo de ACF
description: El cuerpo de ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476595"
---
# <a name="the-acf-body"></a>El cuerpo de ACF

El cuerpo de ACF contiene atributos de configuración que se aplican a los tipos y funciones definidos en el cuerpo de la interfaz del archivo IDL. El cuerpo del ACF puede estar vacío o puede contener atributos de parámetro, función y [**typedef**](/windows/desktop/Midl/typedef)de [**ACF.**](/windows/desktop/Midl/include) Todos estos elementos son opcionales. Los atributos aplicados a tipos y funciones individuales en el cuerpo de ACF invalidan los atributos del encabezado ACF.

El ACF especifica el comportamiento en el equipo local y no afecta a los datos transmitidos a través de la red. Se usa para especificar los detalles de un código auxiliar que se va a generar. En el modo de compatibilidad de DCE ([**/osf**](/windows/desktop/Midl/-osf)), el ACF no afecta a la interacción entre los códigos auxiliares, sino entre el código auxiliar y el código de aplicación.

Un parámetro especificado en el ACF debe ser uno de los parámetros especificados en el archivo IDL. El orden de especificación del parámetro en el ACF no es significativo porque la coincidencia es por nombre, no por posición. La lista de parámetros del ACF puede estar vacía, incluso cuando la lista de parámetros de la firma IDL correspondiente no es (pero no se recomienda). Los declaradores abstractos (parámetros sin nombre) del archivo IDL hacen que el compilador MIDL notime errores al procesar el ACF porque no se encuentra el parámetro.

La directiva **include de** ACF especifica los archivos de encabezado que aparecen en el encabezado generado como parte de una instrucción include estándar del preprocesador **\# C.** La palabra clave ACF **include** difiere de una **\# directiva include.** La palabra  clave include de ACF hace que la línea "**\# include** *filename*" aparezca en el archivo de encabezado generado, mientras que la directiva de lenguaje C "**\# include** *filename*" hace que el contenido de ese archivo se coloque en el ACF.

La instrucción [**typedef de**](/windows/desktop/Midl/typedef) ACF permite aplicar atributos de tipo ACF a los tipos definidos anteriormente en el archivo IDL. La sintaxis de **typedef de** ACF difiere de la sintaxis **de typedef de** C.

Los atributos de función ACF permiten especificar atributos que se aplican a la función en su conjunto. Para obtener más información, **\[** [**vea code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** y **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .

Los atributos de parámetro ACF permiten especificar atributos que se aplican a parámetros individuales de la función. Para obtener más información, vea **\[** [**recuento de \_ bytes.**](/windows/desktop/Midl/byte-count) **\]**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**/app \_ config**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[identificador \_ automático\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[Código\]**](../midl/code.md)
</dt> <dt>

[**\[identificador \_ explícito\]**](../midl/explicit-handle.md)
</dt> <dt>

[El archivo del lenguaje de definición de interfaz (IDL)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[identificador \_ implícito\]**](../midl/implicit-handle.md)
</dt> <dt>

[**incluír**](/windows/desktop/Midl/include)
</dt> <dt>

[Midl](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[Optimizar\]**](../midl/optimize.md)
</dt> <dt>

[**\[representar \_ como\]**](../midl/represent-as.md)
</dt> <dt>

[**Typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 