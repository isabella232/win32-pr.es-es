---
description: Un objeto de rendimiento es una entidad para la que están disponibles los datos de rendimiento.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Diseño de objetos y contadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062892"
---
# <a name="object-and-counter-design"></a>Diseño de objetos y contadores

Un objeto de rendimiento es una entidad para la que están disponibles los datos de rendimiento. Los contadores de rendimiento definen el tipo de datos que está disponible para un objeto de rendimiento. Una aplicación puede proporcionar información para varios objetos de rendimiento. Los objetos de rendimiento pueden contener contadores de instancia única o varios contadores de instancia. Un objeto de instancia única devuelve un único conjunto de valores de contador.

Un objeto de instancia múltiple devuelve una instancia del objeto para cada aparición del objeto que controla la aplicación. Por ejemplo, una aplicación SCSI podría definir un objeto de unidad con dos contadores, como Bytes leídos y Bytes escritos. Cuando el consumidor consulta el objeto, el archivo DLL de rendimiento devuelve una instancia del objeto para cada unidad que controla la aplicación.

Después de decidir si el objeto admite una sola instancia o varias instancias, debe decidir el tipo de contadores que desea que proporcione el objeto. Por ejemplo, puede proporcionar valores de contador que se muestran como valores sin procesar, como tasas o como porcentajes.

Para obtener una lista de los tipos de contador predefinidos entre los que debe elegir, vea la sección Tipos de contador del Kit de implementación de [Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). En función del tipo de contador, puede proporcionar simplemente los datos sin procesar o también puede que tenga que proporcionar información de tiempo y frecuencia, así como datos de contadores adicionales utilizados por el consumidor para calcular un valor que se pueda mostrar.

El método que se usa para recopilar los datos puede ser tan sencillo como incrementar un contador cada vez que se llama a una rutina determinada de la aplicación, o puede implicar cálculos lentos. Los contadores y temporizadores deben incrementarse y nunca borrarse. Los contadores pueden ajustarse, siempre que no se ajusten dos veces entre la muestra del consumidor. La aplicación puede recopilar y almacenar datos durante su ejecución normal, siempre y cuando no afecte a su rendimiento.

Para algunos tipos de datos, puede ser más eficaz o adecuado recopilar los datos a petición. En esta situación, el archivo DLL de rendimiento debe comunicar a la aplicación que se han solicitado los datos. En el caso de los datos que son costosos de recopilar (en términos de tiempo de procesador o uso de memoria), considere la posibilidad de recopilar datos solo cuando el consumidor solicite **datos costosos.** Esto permite a un consumidor solicitar datos de forma rutinaria para todos los contadores que no son costosos. Los datos solo se pueden solicitar cuando sea necesario. La herramienta Rendimiento no recopila **datos costosos.**

 

 
