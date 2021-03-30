---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Usar parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fe8fc7c79ed27c467b59ef67132e816cdcd63
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279869"
---
# <a name="using-parameters"></a>Usar parámetros

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Además de puntuar correctamente una opción que contiene instancias de ParameterRef (consulte [parámetros de referencia](referencing-parameters.md)), los proveedores y clientes de PrintCapabilities o PrintTicket deben estar preparados para controlar las siguientes situaciones en las que intervienen los parámetros.

Los clientes de la interfaz de usuario (IU) deben pedir al usuario que proporcione inicializadores de parámetros (valores para los elementos ParameterInit) para los parámetros designados en el momento adecuado, de modo que se inserten los elementos ParameterInit adecuados en el PrintTicket. Los clientes de la interfaz de usuario deben poder distinguir los dos tipos de parámetros, de manera incondicional y obligatorio condicionalmente, y deben ser capaces de administrar cada tipo adecuadamente. Para un parámetro no condicionalmente obligatorio, la interfaz de usuario debe asegurarse de que se proporciona un elemento ParameterInit para este tipo de parámetro. Para un parámetro obligatorio condicionalmente, la interfaz de usuario debe proporcionar un valor de ParameterInit si se hace referencia al parámetro mediante una opción que está seleccionada en el PrintTicket. El estado obligatorio de un parámetro se especifica en una instancia de ParameterDef. Para obtener más información, vea [elementos ParameterDef y ParameterInit](parameterdef-and-parameterinit-elements.md). Los clientes de la interfaz de usuario deben validar los valores de ParameterInit proporcionados por el usuario para comprobar que cumplen los requisitos especificados en la instancia de ParameterDef.

Los proveedores de PrintTicket también deben comprobar las instancias de ParameterInit proporcionadas por el PrintTicket para comprobar que todos los parámetros necesarios están presentes y que cumplen los requisitos especificados en la instancia de ParameterDef. El código de validación debe proporcionar valores predeterminados razonables en caso de que los valores de ParameterInit no sean válidos o falten. Tenga en cuenta que un ParameterDef permite proporcionar un valor predeterminado para este fin. Además, si hay restricciones que implican a los parámetros, por ejemplo, "Si *CopyCount* es mayor que N, no use una bandeja de entrada de pequeña capacidad", el código de validación de PrintTicket debe detectar esta restricción y modificar el valor de PrintTicket para evitar la activación de la restricción.

Si hay alguna dependencia de PrintCapabilities en los parámetros especificados en el PrintTicket, los proveedores de PrintCapabilities deben supervisar los valores de ParameterInit y generar un documento de PrintCapabilities adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



