---
description: Las cadenas del constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Conceptos de las cadenas del constructor de objetos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998200"
---
# <a name="com-object-constructor-strings-concepts"></a>Conceptos de las cadenas del constructor de objetos COM+

Las cadenas del constructor de objetos COM+ son cadenas de inicialización que se especifican administrativamente para un componente. Puede usar cadenas de constructor de objeto para escribir un único componente con un grado de generalidad que permita que se personalice más adelante para una tarea determinada. es decir, puede realizar la construcción de objetos parametrizados.

Por ejemplo, puede usar esta característica para escribir un componente que contenga una conexión ODBC genérica y, posteriormente, especificar un DSN exacto para el componente de forma administrativa. Si cambia la configuración del sistema, puede cambiar la cadena del constructor en consecuencia.

> [!Note]  
> Las cadenas del constructor de objetos no deben usarse para almacenar información confidencial de seguridad.

 

Puede utilizar cadenas del constructor de objetos junto con la [agrupación de objetos](com--object-pooling.md) para lograr un mayor grado de granularidad en la forma en que agrupa y reutiliza los recursos. Por ejemplo, podría crear varios componentes distintos, idénticos a excepción de las cadenas de constructor y los CLSID, para mantener distintos grupos de objetos que contengan conexiones que puedan usar los distintos grupos de clientes. Esto sería útil si las conexiones se abren de forma que las enlaza a roles de seguridad determinados, como cuando las conexiones se abren con cierta autenticación específica en la base de datos, lo que las representa en el caso general.

Para ello, puede escribir un único componente genérico que se base en cadenas de constructor de objetos, mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), y volver a compilarlo para generar varios componentes personalizables con un CLSID distinto. Después, puede adaptar administrativamente cada componente para abrir una conexión adecuada con una cadena de constructor, configurarlos para que se agrupen y se mantendrán en grupos distintos por CLSID.

Puede especificar una cadena de constructor cuando un componente se ha escrito específicamente para reconocer la cadena que especifique. Los componentes pueden tener acceso mediante programación a estas cadenas mediante [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

Las cadenas de constructor se pasan en el momento de creación del objeto solo cuando la construcción del objeto está habilitada de forma administrativa. COM+ llama al método [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) que implementa. Dentro de ese método, puede tener acceso a la cadena del constructor mediante [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Las cadenas vacías pueden ser entradas válidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agrupación de objetos COM+](com--object-pooling.md)
</dt> <dt>

[Especificar una cadena de constructor de objeto para un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Usar una cadena de constructor de objeto para construir un componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



