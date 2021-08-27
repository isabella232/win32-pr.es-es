---
description: Las aplicaciones COM+ constan de uno o varios componentes COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Partes de una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f08e9e73146f2d15e70be1cb72f847003f54ac510834f86501a7f1964ad14ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812893"
---
# <a name="parts-of-a-com-application"></a>Partes de una aplicación COM+

Las aplicaciones COM+ constan de uno o varios componentes COM.

Los siguientes términos se usan en toda la documentación de COM+:

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*
</dt> <dd>

Unidad binaria de código que crea objetos COM (incluye código de empaquetado y registro).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objeto COM*
</dt> <dd>

Instancia de una clase COM.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Clase COM*
</dt> <dd>

Implementación concreta con nombre de una o varias interfaces. Una clase COM se identifica mediante un CLSID (a veces también mediante un ProgID).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interfaz COM*
</dt> <dd>

Grupo de funciones de método relacionadas expuestas por una clase COM que especifican un contrato. Esto incluye el nombre, la firma de interfaz, la semántica de la interfaz y el formato de búfer de serialización. Una interfaz se identifica mediante un IID. La sintaxis de la interfaz se define en bibliotecas de tipos o IDL. Las interfaces de una clase COM deben dividirse en conjuntos de métodos fáciles de administrar y cohesivos.

Las interfaces COM son inmutables; el contrato COM indica que no se pueden modificar. Cualquier modificación (como agregar métodos) requiere definir una nueva interfaz.

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Método COM*
</dt> <dd>

Una de las funciones relacionadas proporcionadas por una interfaz COM.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Componentes configurados y no configurados

Para aprovechar los servicios que admiten las aplicaciones COM+, el entorno COM+ impone requisitos específicos en los componentes COM creados para aplicaciones COM+. Cuando se agrega a una aplicación COM+, un componente COM se conoce como *componente configurado.*

Los componentes COM creados para aplicaciones COM+ son componentes de servidor en proceso. El componente debe contener una biblioteca de tipos (archivo .tlb) para describir todas las clases implementadas en el componente y declarar las interfaces en todas las clases del componente. Puede crear e implementar estos componentes con Microsoft Visual Basic, Microsoft Visual C++ o cualquier herramienta de desarrollo compatible con COM.

Un *componente no configurado es* un componente que no está instalado en una aplicación COM+. Puede transformar la mayoría de los componentes no configurados en componentes configurados simplemente integrándolos en una aplicación COM+.

> [!Note]  
> No use el mismo AppID para una aplicación COM+ y en el Registro para un componente no configurado. Cuando se activa el componente no configurado , ya que la activación puede recuperar la información de la aplicación COM+ del Registro que no contiene la información necesaria para la activación COM. Podrían surgir problemas similares si se realiza una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) desde DllHost que hospeda la aplicación de servidor COM+.

 

 

 
