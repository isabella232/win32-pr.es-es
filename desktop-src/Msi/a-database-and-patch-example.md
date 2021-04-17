---
description: Una aplicación puede usar la función MsiOpenDatabase para abrir una base de datos de instalación nueva o existente (archivo. msi) o un paquete de revisión (archivo. msp). La aplicación comprueba el valor devuelto de MsiOpenDatabase antes de utilizar el identificador de base de datos.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Un ejemplo de base de datos y revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667075"
---
# <a name="a-database-and-patch-example"></a>Un ejemplo de base de datos y revisión

Una aplicación puede usar la función [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir una base de datos de instalación nueva o existente (archivo. msi) o un paquete de revisión (archivo. msp). La aplicación comprueba el valor devuelto de **MsiOpenDatabase** antes de utilizar el identificador de base de datos.

En los ejemplos siguientes se usan las variables de tipo **PMSIHANDLE** definidas en MSI. h. Se recomienda usar el tipo **PMSIHANDLE** porque el instalador cierra los objetos **PMSIHANDLE** cuando salen del ámbito, mientras que la aplicación debe cerrar los objetos **MSIHANDLE** llamando a [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Para obtener más información, consulte la sección [uso de PMSIHANDLE en lugar de Handle](windows-installer-best-practices.md) en el [Windows Installer procedimientos recomendados](windows-installer-best-practices.md).

En el ejemplo siguiente se abre una base de datos, sample.msi, solo para lectura. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) se ejecuta solo si sample.msi existe en el directorio c: \\ Test. Cuando se realiza correctamente, el identificador de base de datos devuelto se puede usar para consultar los datos del paquete de instalación mediante [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) y [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



En el ejemplo siguiente se abre la base de datos para lectura y escritura. Si la aplicación llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), se guardan todos los cambios realizados en la base de datos. Si la aplicación no llama a **MsiDatabaseCommit**, no se realiza ningún cambio en la base de datos.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



En el ejemplo siguiente se toma una base de datos existente, se text.msi y se crea una nueva base de datos, newtest.msi. Cualquier cambio que se realice se puede guardar en la nueva base de datos mediante una llamada a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). La base de datos existente especificada en el parámetro *szDatabasePath* no cambia.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



En el ejemplo siguiente se abre un paquete de revisión de Windows Installer (archivo. msp) para lectura solamente. El identificador de revisión devuelto se puede usar para determinar los contenedores y los subalmacenamientos de transformación incluidos en el paquete de revisión mediante consultas en las tablas [ \_ streams](-streams-table.md) y [ \_ Storages](-storages-table.md) .

**Windows Installer 2,0:** No compatible. A partir de Windows Installer 3,0, la aplicación puede consultar la [tabla MsiPatchSequence](msipatchsequence-table.md) presente en un paquete de revisión que utiliza la nueva información de secuencia de revisión.


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



