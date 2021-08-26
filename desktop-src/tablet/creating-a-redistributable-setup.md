---
description: Para distribuir una aplicación habilitada para entrada de lápiz a equipos que no ejecutan Windows Vista o Windows XP Tablet PC Edition 2005 (es decir, equipos que ejecutan Windows XP, Windows Server 2003 o Windows 2000), debe incluir los módulos de combinación necesarios en la instalación.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Creación de una instalación redistribuible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bdd63a00f1f4245ea83173e1a7e609094fe30e5357f5e1ebf3d6da63182cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936875"
---
# <a name="creating-a-redistributable-setup"></a>Creación de una instalación redistribuible

Para distribuir una aplicación habilitada para entrada de lápiz a equipos que no ejecutan Windows Vista o Windows XP Tablet PC Edition 2005 (es decir, equipos que ejecutan Windows XP, Windows Server 2003 o Windows 2000), debe incluir los módulos de combinación necesarios en la instalación.

El módulo de combinación Mstpcrt.msm incluye todos los archivos, recursos, entradas del Registro y lógica de configuración necesarios para que Windows Installer instale los archivos compartidos que otras plataformas necesitan para ejecutar aplicaciones no administradas desarrolladas para tablet PC. Mstpcrt.msm lo consumen los Windows Installer (.msi). Para las aplicaciones que usan [**el objeto InkDivider,**](inkdivider-class.md) también debe redistribuir InkDiv.msm. En el caso de las aplicaciones que usan componentes administrados, también debe incluir los archivos de módulo de combinación para esos componentes administrados.

En la tabla siguiente se describen los archivos de módulo de combinación que se envían con el kit de desarrollo de software (SDK) Windows XP Tablet PC Edition.



| Módulo de combinación redistribuible | Descripción                                                                                                                    | Archivos                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv.msm<br/>        | Instala la versión no administrada del [**objeto InkDivider.**](inkdivider-class.md)<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt.msm<br/>       | Instala los componentes no administrados de la versión 1.0 de tablet PC Platform.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60.msm<br/>       | Instala los componentes del entorno Microsoft Visual C++ ejecución.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt.msm<br/>        | Instala componentes del entorno de ejecución de Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17.msm<br/>      | Instala los componentes administrados del entorno de ejecución de la plataforma de Tablet PC. Requiere que el archivo mstpcrt.msm esté instalado.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM.msm<br/>         | Instala los componentes de Automation de InkAnalysis API.<br/>                                                          | IACom.dll<br/>                                        |
| iacore.msm<br/>        | Instala los componentes de clase base de InkAnalysis API.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm.msm<br/>      | Instala los componentes de la biblioteca administrada de InkAnalysis API.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX.msm<br/>       | Instala los componentes Windows Presentation Foundation de InkAnalysis API.<br/>                                     | IAWinFX.dll<br/>                                      |
| journal.msm<br/>       | Instala los componentes del Lector de diario.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom.msm<br/>        | Instala los componentes de Automation del espacio de nombres StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Para usar la funcionalidad de Microsoft .NET Framework que se incluye en los módulos de combinación para los componentes administrados, debe tener instalado Service Pack 2 de Framework en el equipo de destino.

 

## <a name="reduced-feature-set"></a>Conjunto de características reducido

Las aplicaciones habilitadas para lápiz tratan los eventos del mouse como movimientos de lápiz para simular el trabajo con un lápiz de tableta. Los usuarios pueden agregar entrada manuscrita, borrarla y guardar documentos de entrada manuscrita. Sin embargo, el reconocimiento y los gestos no están disponibles para usuarios distintos de los que ejecutan Windows XP Tablet PC Edition.

Mstpcrt.msm no incluye Windows de entrada del equipo de tableta o de diario.

El [**objeto PenInputPanel**](peninputpanel-class.md) no funciona en ningún sistema operativo además de Windows XP Tablet PC Edition.

## <a name="deployment"></a>Implementación

> [!Note]  
> Si la aplicación usa código administrado, también debe implementar framework. El marco debe instalarse antes de que se instalen los ensamblados administrados de Tablet PC.

 

Para incluir Mstpcrt.msm en un Microsoft Visual Studio de instalación de .NET:

1.  En la Explorador de soluciones, seleccione el proyecto de instalación.
2.  En el menú Project, haga clic **en Agregar** y, a continuación, haga clic en Módulo **de mezcla**.
    > [!Note]  
    > También puede acceder  al cuadro de diálogo Agregar módulos haciendo clic con el botón derecho en el nombre del proyecto del instalador en la Explorador de soluciones, haciendo clic en Agregar y, a continuación, **seleccionando Combinar módulo**.

     

3.  En el **cuadro de diálogo** Agregar módulos, vaya a Y seleccione **Mstpcrt.msm**.
4.  Haga clic en **Abrir**.

Mstpcrt.msm se agrega al proyecto de instalación y aparece en Explorador de soluciones ventana.

Windows El instalador agrega los archivos contenidos en el módulo de combinación a la carpeta Archivos de programa. Para usar estos archivos, los usuarios finales deben iniciar sesión con una cuenta que tenga acceso a la carpeta Archivos de programa.

> [!Note]  
> Debe agregar las [acciones Acción SelfRegModules y](../msi/selfregmodules-action.md) Acción [SelfUnregModules](../msi/selfunregmodules-action.md) a la secuencia de instalación. Las [acciones MsiPublishAssemblies Action](../msi/msipublishassemblies-action.md) y [MsiUnpublishAssemblies Action](/windows/desktop/Msi/msiunpublishassemblies-action) reciben su orden en la secuencia de instalación de estas acciones.

 

 

