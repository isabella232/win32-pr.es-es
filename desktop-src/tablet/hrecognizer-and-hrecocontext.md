---
description: Se hace referencia a un reconocedor de tinta con un identificador de HRECOGNIZER y un contexto de reconocedor como identificador de HRECOCONTEXT. Una biblioteca de vínculos dinámicos (DLL) del reconocedor puede implementar reconocedores para más de un idioma.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER y HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715247"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER y HRECOCONTEXT

Se hace referencia a un reconocedor de tinta con un identificador de [HRECOGNIZER](hrecognizer-handle.md) y un contexto de reconocedor como identificador de [HRECOCONTEXT](hrecocontext-handle.md) .

Una biblioteca de vínculos dinámicos (DLL) del reconocedor puede implementar reconocedores para más de un idioma. Si es así, cada idioma se selecciona mediante un CLSID que se pasa al crear el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) en la aplicación. Además, una DLL de reconocedor puede crear varios identificadores de reconocedor cuando se carga, uno o varios de los lenguajes reconocidos.

Se crea un contexto de reconocedor que representa el evento de reconocimiento de una parte específica de la entrada de lápiz. Cuando se crea el contexto, se pasa el identificador de objetos del reconocedor asociado a la función [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) . Esto asocia el idioma con el contexto del reconocedor.

Un contexto de reconocedor puede representar el reconocimiento de toda la tinta en el cuerpo de un correo electrónico, la tinta de un solo campo dentro de una aplicación o una sola línea de texto escrita en el panel de entrada de Tablet PC. El volumen de tinta de un único contexto de reconocedor puede variar de un solo trazo a una página completa o más.

El contexto del reconocedor se define mediante la configuración de:

-   La guía de reconocimiento.
-   Cualquier Factoids.
-   Cualquier marcador.
-   Contexto del texto.
-   Cualquier lista de palabras.
-   El modo de autocompletar caracteres.

El identificador del contexto del reconocedor se pasa a todas las funciones que usan esta configuración. Cambiar un valor de configuración cambia el contexto del reconocedor.

La aplicación puede usar varios contextos para reconocer la tinta de diferentes partes de la pantalla. Un contexto individual puede reconocer varias líneas de texto. Sin embargo, un contexto individual no puede procesar dos párrafos escritos en paralelo, como varias columnas en un artículo de un periódico.

Para reconocer nuevas entradas manuscritas, cree un nuevo contexto. Como alternativa, utilice la función [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) para realizar una copia de un contexto que no tenga la tinta y los resultados, o la función [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) para borrar un contexto de su tinta y resultados. Con estos enfoques, una aplicación de entrada manuscrita puede reutilizar un contexto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SetGuide función)**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**GetGuide función)**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**SetFactoid función)**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**Función SetFlags**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**SetEnabledUnicodeRanges función)**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges función)**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**SetCACMode función)**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**SetTextContext función)**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**SetWordList función)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



