---
description: Las aplicaciones COM+ constan de uno o varios componentes COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Partes de una aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496025"
---
# <a name="parts-of-a-com-application"></a>Partes de una aplicación COM+

Las aplicaciones COM+ constan de uno o varios componentes COM.

Los siguientes términos se utilizan en toda la documentación de COM+:

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*
</dt> <dd>

Unidad binaria de código que crea objetos COM (incluye el código de empaquetado y de registro).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objeto COM*
</dt> <dd>

Instancia de una clase COM.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Clase COM*
</dt> <dd>

Una implementación concreta y con nombre de una o más interfaces. Una clase COM se identifica mediante un CLSID (a veces también mediante un ProgID).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interfaz COM*
</dt> <dd>

Grupo de funciones de método relacionadas expuestas por una clase COM que especifica un contrato. Esto incluye el nombre, la firma de la interfaz, la semántica de la interfaz y el formato del búfer de serialización. Un IID identifica una interfaz. La sintaxis de la interfaz se define en las bibliotecas de tipos y de IDL. Las interfaces de una clase COM se deben dividir en conjuntos de métodos coherentes y administrables.

Las interfaces COM son inmutables; el contrato COM indica que no se pueden modificar. Cualquier modificación (como agregar métodos) requiere la definición de una nueva interfaz.

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Método COM*
</dt> <dd>

Uno de un conjunto de funciones relacionadas proporcionadas por una interfaz COM.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Componentes configurados y no configurados

Para sacar partido de los servicios que admiten las aplicaciones COM+, el entorno COM+ impone requisitos específicos en los componentes COM compilados para aplicaciones COM+. Cuando se agrega a una aplicación COM+, un componente COM se conoce como *componente configurado*.

Los componentes COM compilados para aplicaciones COM+ son componentes de servidor en proceso. El componente debe contener una biblioteca de tipos (archivo. tlb) para describir todas las clases implementadas en el componente y declarar las interfaces en todas las clases del componente. Puede crear e implementar estos componentes con Microsoft Visual Basic, Microsoft Visual C++ o cualquier herramienta de desarrollo compatible con COM.

Un *componente no configurado* es un componente que no está instalado en una aplicación com+. Puede transformar la mayoría de los componentes no configurados en componentes configurados simplemente mediante su integración en una aplicación COM+.

> [!Note]  
> No use el mismo AppID para una aplicación COM+ y en el registro para un componente sin configurar. Cuando se activa el componente sin configurar, como activación puede recuperar la información de la aplicación COM+ del registro que no contiene la información necesaria para la activación COM. Pueden surgir problemas similares si se realiza una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) desde Dllhost que hospeda la aplicación de servidor com+.

 

 

 
