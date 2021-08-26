---
description: Las cadenas de constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceptos de cadenas de constructor de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baef62780950e93043a48c2ccf13910faf7c692dc534f984ffd028e0b342dcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029525"
---
# <a name="com-object-constructor-strings-concepts"></a>Conceptos de cadenas de constructor de objetos COM+

Las cadenas de constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente. Puede usar cadenas de constructor de objetos para escribir un único componente con un grado de generalidad que permita personalizarlo posteriormente para una tarea determinada; es decir, puede realizar la construcción de objetos con parámetros.

Por ejemplo, puede usar esta característica para escribir un componente que contiene una conexión ODBC genérica y, posteriormente, especificar un DSN exacto para el componente administrativamente. Si cambia la configuración del sistema, puede cambiar la cadena del constructor en consecuencia.

> [!Note]  
> Las cadenas de constructor de objetos no deben usarse para almacenar información confidencial de seguridad.

 

Puede usar cadenas de constructor [](com--object-pooling.md) de objetos junto con la agrupación de objetos para lograr un mayor grado de granularidad en la forma de agrupación y reutilización de recursos. Por ejemplo, puede crear varios componentes distintos, idénticos excepto las cadenas de constructor y CLID, para mantener distintos grupos de objetos que mantienen conexiones utilizables por grupos distintos de clientes. Esto sería útil si las conexiones se abren de una manera que las enlaza a determinados roles de seguridad, como cuando las conexiones se abren con alguna autenticación específica en la base de datos, lo que las hace no reutilizables en el caso general.

Para ello, puede escribir un único componente genérico que se base en cadenas de constructor de objetos mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)y volver a compilarlo para generar varios componentes personalizables cada uno con un CLSID distinto. A continuación, puede adaptar administrativamente cada componente para abrir una conexión adecuada con una cadena de constructor, configurarlos para que se agruparán y se mantendrán en grupos distintos por CLSID.

Puede especificar una cadena de constructor cuando se ha escrito un componente específicamente para reconocer la cadena que especifique. Los componentes pueden acceder a estas cadenas mediante programación mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

Las cadenas de constructor se pasan en el momento de la creación del objeto solo cuando la construcción de objetos está habilitada administrativamente. COM+ llama al [**método IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que implementa. Dentro de ese método, puede acceder a la cadena de constructor mediante [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Las cadenas vacías pueden ser entradas válidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agrupación de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Especificar una cadena de constructor de objetos para un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Usar una cadena de constructor de objetos para construir un componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



