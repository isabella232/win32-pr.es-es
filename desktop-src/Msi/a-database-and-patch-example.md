---
description: Una aplicación puede usar la función MsiOpenDatabase para abrir una base de datos de instalación nueva o existente (.msi archivo) o un paquete de revisión (archivo .msp). La aplicación comprueba el valor devuelto de MsiOpenDatabase antes de usar el identificador de base de datos.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Ejemplo de base de datos y revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159281"
---
# <a name="a-database-and-patch-example"></a>Ejemplo de base de datos y revisión

Una aplicación puede usar la [**función MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) para abrir una base de datos de instalación nueva o existente (.msi archivo) o un paquete de revisión (archivo .msp). La aplicación comprueba el valor devuelto de **MsiOpenDatabase antes** de usar el identificador de base de datos.

En los ejemplos siguientes se usan las variables de tipo **PMSIHANDLE** definidas en msi.h. Se recomienda usar el tipo **PMSIHANDLE** porque el instalador cierra objetos **PMSIHANDLE** a medida que sale del ámbito, mientras que la aplicación debe cerrar objetos **MSIHANDLE** llamando a [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Para obtener más información, [vea la sección Use PMSIHANDLE instead of HANDLE (Usar PMSIHANDLE en](windows-installer-best-practices.md) lugar de HANDLE) en Windows Installer Best Practices (Procedimientos [recomendados del instalador).](windows-installer-best-practices.md)

En el ejemplo siguiente se abre una base de sample.msi, solo para lectura. [**MsiOpenDatabase solo**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) se realiza correctamente si sample.msi existe en el directorio de prueba \\ c:. Si se ejecuta correctamente, el identificador de base de datos devuelto se puede usar para consultar los datos del paquete de instalación mediante [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) y [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



En el ejemplo siguiente se abre la base de datos para leer y escribir. Si la aplicación llama a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), se guardan todos los cambios realizados en la base de datos. Si la aplicación no llama a **MsiDatabaseCommit,** no se realiza ningún cambio en la base de datos.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



En el ejemplo siguiente se toma una base de datos existente, text.msi, y se crea una nueva base de datos, newtest.msi. Los cambios que se realicen se pueden guardar en la nueva base de datos mediante una llamada a [**MsiDatabaseCommit.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) La base de datos existente especificada en el *parámetro szDatabasePath* no cambia.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



En el ejemplo siguiente se abre Windows paquete de revisión del instalador (archivo .msp) solo para lectura. El identificador de revisión devuelto se puede usar para determinar los archivadores y transformar los subalmacenamientos incluidos en el paquete de revisión mediante consultas en las [ \_ tablas Secuencias](-streams-table.md) [ \_ y Storages.](-storages-table.md)

**Windows Installer 2.0:** No se admite. A partir Windows Installer 3.0, la aplicación puede consultar la tabla [MsiPatchSequence](msipatchsequence-table.md) presente en un paquete de revisión que usa la nueva información de secuenciación de revisiones.


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



 

 



