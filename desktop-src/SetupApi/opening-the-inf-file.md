---
description: Debe usar la función SetupOpenInfFile para abrir el archivo INF para poder recuperar información de él o para anexar otros archivos INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Abrir el archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910337"
---
# <a name="opening-the-inf-file"></a>Abrir el archivo INF

Debe usar la función [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) para abrir el archivo INF para poder recuperar información de él o para anexar otros archivos INF.

Lo siguiente abre un archivo INF mediante [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) y devuelve un identificador, MyInf, al archivo INF abierto. El parámetro *InfClass* de **SetupOpenInfFile** se especifica como **null** para indicar que la clase del archivo inf debe omitirse.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



Después de abrir un archivo INF, puede llamar a la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) para anexar un archivo al archivo INF abierto. Para anexar varios archivos, repita este proceso. Si llama a la función **SetupOpenAppendInfFile** y el nombre de archivo que se le ha pasado es **null**, la función buscará en la sección de versión del archivo INF abierto (y los archivos INF anexados) una clave LayoutFile. Si la función encuentra una clave, anexará el archivo especificado por esa clave (normalmente, el diseño. INF). Cuando se han combinado varios archivos INF, **SetupOpenAppendInfFile** comienza con el último archivo INF anexado cuando busca una sección de versión.

 

 



