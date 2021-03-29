---
title: Intervalos
description: Intervalos
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Services Framework (TSF), intervalos
- TSF (marco de trabajo de servicios de texto), intervalos
- servicios de texto, intervalos
- Aplicaciones habilitadas para TSF, intervalos
- ranges
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- servicios de texto, delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
- Marco de trabajo de servicios de texto (TSF), clones
- TSF (marco de trabajo de servicios de texto), clones
- servicios de texto, clones
- Aplicaciones habilitadas para TSF, clones
- clones
- Text Services Framework (TSF), copias de seguridad
- TSF (marco de trabajo de servicios de texto), copias de seguridad
- servicios de texto, copias de seguridad
- Aplicaciones habilitadas para TSF, copias de seguridad
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994568"
---
# <a name="ranges"></a>Intervalos

## <a name="anchors"></a>Delimitadores

Un intervalo está delimitado por dos *delimitadores*, un delimitador inicial y un delimitador final. Existe un delimitador en una ranura imaginaria entre dos caracteres. El delimitador de inicio se relaciona con el texto que sigue al delimitador y el delimitador final se relaciona con el texto que precede al delimitador. Los delimitadores inicial y final pueden existir en la misma ubicación. En este caso, el intervalo tiene una longitud de cero.

Por ejemplo, empiece con el texto siguiente:


```C++
This is text.
```



Ahora aplique un intervalo a este texto con los delimitadores inicial y final en la posición 0. Se representa visualmente como:


```C++
<anchor></anchor>This is text.
```



Los delimitadores no ocupan espacio en el propio texto. Este es un intervalo de longitud cero y su texto está vacío.

Ahora, desplace el anclaje final + 3 posiciones. Se representa visualmente como:


```C++
<anchor>Thi</anchor>s is text.
```



El delimitador inicial se coloca justo delante del carácter en la posición 0 y el delimitador final se coloca justo después del carácter de la posición 3 porque el delimitador final se desplazó a los 3 lugares correctos. El intervalo de texto es ahora "Thi".

Además, no se puede hacer que el delimitador de inicio siga el delimitador final y no se puede establecer el delimitador final para que preceda al delimitador inicial.

## <a name="anchor-gravity"></a>Gravedad del anclaje

Cada delimitador tiene un valor de *gravedad* que determina cómo responde el delimitador cuando se inserta texto en la secuencia de texto en la posición del delimitador. Cuando se realiza una inserción en la posición de un delimitador, se debe realizar un ajuste en la posición del delimitador. La gravedad determina cómo se realiza este ajuste de posición de delimitador.

Por ejemplo:


```C++
It is <anchor></anchor>cold today.
```



Si la palabra "Very" se inserta en la posición del intervalo, el delimitador inicial puede colocarse antes o después de la palabra insertada:


```C++
It is <anchor>very </anchor>cold today.
```



\- O bien


```C++
It is very <anchor></anchor>cold today.
```



La gravedad del anclaje especifica cómo se cambia la posición del delimitador cuando se realiza una inserción en su posición. La gravedad puede ser *hacia atrás* o *hacia delante*.

Si el delimitador tiene gravedad anterior, el delimitador se desplaza hacia atrás, con respecto al punto de inserción, en la inserción para que el texto insertado siga el delimitador:


```C++
It is <anchor>very </anchor>cold today.
```



Si el delimitador tiene gravedad de avance, el delimitador se desplaza hacia delante (en relación con el punto de inserción) en la inserción para que el texto insertado preceda al delimitador:


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Clones y copias de seguridad

Hay dos formas de hacer una "copia" de un objeto de intervalo. El primero es crear un *clon* del intervalo mediante [ITfRange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone). La segunda consiste en realizar una *copia de seguridad* del intervalo mediante [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).

Un clon es una copia de un intervalo que no incluye datos estáticos. Los delimitadores del intervalo se copian, pero el clon todavía cubre un intervalo de texto dentro del contexto. Un clon es un objeto de intervalo en todos los aspectos. Esto significa que el texto y las propiedades de un intervalo clonado son dinámicos y cambiarán si cambia el texto o las propiedades del intervalo que abarca el clon.

Una copia de seguridad almacena el texto y las propiedades de un intervalo en el momento en que se realiza la copia de seguridad como datos estáticos. Una copia de seguridad también clona el intervalo original para que se pueda realizar un seguimiento de los cambios en el tamaño y la posición del intervalo original. Esto significa que el texto y las propiedades de un intervalo del que se ha realizado una copia de seguridad son estáticos y no cambian si cambia el texto o las propiedades del intervalo que abarca la copia de seguridad.

Por ejemplo, el intervalo siguiente (pRange) en el contexto:


```C++
"This is some <pRange>text</pRange>."
```



Ahora cree un clon y una copia de seguridad de este intervalo:


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



Ahora, los objetos contienen lo siguiente:


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Ahora cambie el texto de pRange:


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



Ahora, los objetos contienen lo siguiente:


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



Al establecer el texto, el texto del contexto debe cambiar. También causó el cambio del delimitador final de pRange y pClone. pClone Now contiene "otras palabras" porque el texto cambió dentro del intervalo y todos los intervalos realizan el seguimiento de estos cambios. Cuando cambia el texto incluido en pRange y pClone, el texto de pClone también cambia.

El texto de pBackup no ha cambiado con respecto a la pRange original porque los datos (texto y propiedades) de la copia de seguridad no están relacionados con el contexto y se almacenan por separado. El clon contenido en la copia de seguridad cambia realmente, pero los datos son estáticos.

Al restaurar una copia de seguridad, la copia de seguridad se puede aplicar al clon dentro de la copia de seguridad o a un intervalo diferente completamente. Para aplicar la copia de seguridad al clon dentro de la copia de seguridad, pase **null** a [ITfRangeBackup:: restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) como se muestra en el ejemplo de código siguiente:


```C++
pBackup->Restore(ec, NULL);
```



Ahora, los objetos contienen lo siguiente:


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Para restaurar la copia de seguridad en un intervalo diferente, pase un puntero al objeto de intervalo al llamar a **ITfRangeBackup:: restore**. El texto y las propiedades de las copias de seguridad se aplicarán al nuevo intervalo. Por ejemplo, si usa el ejemplo anterior antes de la llamada a **restore** , pRange se modificará para demostrar esto:


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



Ahora, los objetos contienen lo siguiente:


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Cuando el delimitador final de pRange se ha desplazado a la izquierda dos lugares, el delimitador final de pClone no cambió.

Ahora restaure la copia de seguridad con pRange con el siguiente ejemplo de código:


```C++
pBackup->Restore(ec, pRange);
```



Ahora, los objetos contienen lo siguiente:


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



El texto que se incluye en pRange se ha reemplazado por "Text", una parte del texto que incluye pClone ha cambiado y pBackup cambia para coincidir con pRange.

 

 




