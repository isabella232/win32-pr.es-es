---
description: Un objeto de rendimiento es una entidad para la que los datos de rendimiento están disponibles.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Diseño de objetos y contadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001976"
---
# <a name="object-and-counter-design"></a>Diseño de objetos y contadores

Un objeto de rendimiento es una entidad para la que los datos de rendimiento están disponibles. Los contadores de rendimiento definen el tipo de datos que están disponibles para un objeto de rendimiento. Una aplicación puede proporcionar información para varios objetos de rendimiento. Los objetos de rendimiento pueden contener contadores de una sola instancia o varios contadores de instancias. Un objeto de instancia única devuelve un único conjunto de valores de contador.

Un objeto de varias instancias devuelve una instancia del objeto para cada repetición del objeto que controla la aplicación. Por ejemplo, una aplicación SCSI podría definir un objeto de unidad con dos contadores, como bytes leídos y bytes escritos. Cuando el consumidor consulta el objeto, el archivo DLL de rendimiento devuelve una instancia del objeto para cada unidad que controla la aplicación.

Después de decidir si el objeto admite una o varias instancias, debe decidir el tipo de contadores que desea que proporcione el objeto. Por ejemplo, puede proporcionar valores de contador que se muestran como valores sin formato, como tasas o como porcentajes.

Para obtener una lista de tipos de contadores predefinidos que debe elegir, consulte la sección tipos de contadores del [Kit de implementación de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). Dependiendo del tipo de contador, es posible que simplemente proporcione los datos sin procesar o que también tenga que proporcionar información de hora y frecuencia y datos de contador adicionales usados por el consumidor para calcular un valor que se pueda mostrar.

El método que se usa para recopilar los datos puede ser tan sencillo como incrementar un contador cada vez que se llama a una rutina determinada de la aplicación, o puede implicar cálculos que consumen mucho tiempo. Los contadores y temporizadores deben incrementarse y nunca deben borrarse. Los contadores se pueden ajustar, siempre y cuando no se ajusten dos veces entre el consumidor. La aplicación puede recopilar y almacenar datos durante su ejecución normal, siempre y cuando no afecte a su rendimiento.

En el caso de algunos tipos de datos, puede ser más eficaz o adecuado recopilar los datos a petición. En esta situación, el archivo DLL de rendimiento debe comunicarse con la aplicación para la que se han solicitado los datos. En el caso de los datos que son caros de recopilar (en términos de tiempo de procesador o uso de memoria), considere la posibilidad de recopilar datos solo cuando el consumidor solicite datos **costosos** . Esto permite a un consumidor solicitar datos de forma rutinaria para todos los contadores que no son costosos. Los datos se pueden solicitar solo cuando sea necesario. La herramienta rendimiento no recopila datos **costosos** .

 

 
