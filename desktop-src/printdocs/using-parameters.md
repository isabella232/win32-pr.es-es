---
description: Aprenda a usar parámetros en un documento PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Usar parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6417a6d30716cf19d22773c28dbf471e75f967d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119400"
---
# <a name="using-parameters"></a>Usar parámetros

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Además de puntuar correctamente una opción que contiene instancias parameterRef (vea Parámetros de [referencia),](referencing-parameters.md)los proveedores y clientes PrintCapabilities o PrintTicket deben estar preparados para controlar las siguientes situaciones que implican parámetros.

Los clientes de la interfaz de usuario (UI) deben solicitar al usuario que proporcione inicializadores de parámetros (valores para los elementos ParameterInit) para los parámetros designados en el momento adecuado para que los elementos ParameterInit adecuados se inserten en PrintTicket. Los clientes de interfaz de usuario deben ser capaces de distinguir los dos tipos de parámetros, obligatorios incondicionalmente y condicionalmente obligatorios, y deben ser capaces de controlar cada tipo correctamente. Para un parámetro incondicionalmente obligatorio, la interfaz de usuario debe asegurarse de que se proporciona un elemento ParameterInit para este tipo de parámetro. Para un parámetro condicionalmente obligatorio, la interfaz de usuario debe proporcionar un valor ParameterInit si una opción seleccionada en PrintTicket hace referencia al parámetro. El estado Obligatorio de un parámetro se especifica en una instancia de ParameterDef. Para obtener más información, [vea ParameterDef y ParameterInit Elements](parameterdef-and-parameterinit-elements.md). Los clientes de interfaz de usuario deben validar los valores ParameterInit proporcionados por el usuario para comprobar que cumplen los requisitos especificados en la instancia parameterDef.

Los proveedores de PrintTicket también deben comprobar las instancias de ParameterInit proporcionadas por PrintTicket para comprobar que todos los parámetros necesarios están presentes y que cumplen los requisitos especificados en la instancia parameterDef. El código de validación debe proporcionar valores predeterminados razonables en caso de que los valores ParameterInit no sean válidos o falte. Observe que parameterDef permite proporcionar un valor predeterminado para este propósito. Además, si hay restricciones que implican los parámetros, por ejemplo, "si *CopyCount* es mayor que N, no use un pequeño cubo de entrada de capacidad", el código de validación de PrintTicket debe detectar esta restricción y modificar printTicket para evitar activar la restricción.

Si hay alguna dependencia de PrintCapabilities en los parámetros especificados en PrintTicket, los proveedores de PrintCapabilities deben supervisar los valores ParameterInit y generar un documento PrintCapabilities adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



