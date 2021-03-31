---
title: Identificadores de tipo de anotación (UIAutomationClient. h)
description: En este tema se describen las constantes con nombre que se utilizan para identificar los tipos de anotaciones de un documento.
ms.assetid: 46948B7C-EC9F-4B55-B769-62EE8BE11D33
topic_type:
- apiref
api_name:
- AnnotationType_AdvancedProofingIssue
- AnnotationType_Author
- AnnotationType_CircularReferenceError
- AnnotationType_Comment
- AnnotationType_ConflictingChange
- AnnotationType_DataValidationError
- AnnotationType_DeletionChange
- AnnotationType_EditingLockedChange
- AnnotationType_Endnote
- AnnotationType_ExternalChange
- AnnotationType_Footer
- AnnotationType_Footnote
- AnnotationType_FormatChange
- AnnotationType_FormulaError
- AnnotationType_GrammarError
- AnnotationType_Header
- AnnotationType_Highlighted
- AnnotationType_InsertionChange
- AnnotationType_Mathematics
- AnnotationType_MoveChange
- AnnotationType_SpellingError
- AnnotationType_TrackChanges
- AnnotationType_Unknown
- AnnotationType_UnsyncedChange
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb628c8e6ada93546291cd9afb87c3194798b9f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800932"
---
# <a name="annotation-type-identifiers"></a>Identificadores de tipo de anotación

En este tema se describen las constantes con nombre que se utilizan para identificar los tipos de anotaciones de un documento.



| Constante o valor                                                                                                                                                                                                                                                                                                                                           | Descripción                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**AnnotationType \_ AdvancedProofingIssue**</dt> <dt>60020</dt> </dl>     | Un problema de prueba avanzado.<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**AnnotationType \_ Autor**</dt> <dt>60019</dt> </dl>                                                                 | Autor del documento.<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**AnnotationType \_ CircularReferenceError**</dt> <dt>60022</dt> </dl> | Error de referencia circular que se ha producido.<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**AnnotationType \_ Comentario**</dt> <dt>60003</dt> </dl>                                                             | Comentario. Los comentarios pueden tomar diferentes formas en función de la aplicación.<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**AnnotationType \_ ConflictingChange**</dt> <dt>60018</dt> </dl>                     | Un cambio conflictivo realizado en el documento.<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**AnnotationType \_ DataValidationError**</dt> <dt>60021</dt> </dl>             | Error de validación de datos que se ha producido.<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**AnnotationType \_ DeletionChange**</dt> <dt>60012</dt> </dl>                                 | Cambio de eliminación realizado en el documento.<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**AnnotationType \_ EditingLockedChange**</dt> <dt>60016</dt> </dl>             | Cambio de edición bloqueado que se realizó en el documento.<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**AnnotationType \_ Nota al final**</dt> <dt>60009</dt> </dl>                                                             | La nota al final de un documento.<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**AnnotationType \_ ExternalChange**</dt> <dt>60017</dt> </dl>                                 | Cambio externo realizado en el documento.<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**AnnotationType \_ Pie de página**</dt> <dt>60007</dt> </dl>                                                                 | Pie de página de una página de un documento.<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**AnnotationType \_ Nota al pie**</dt> <dt>60010</dt> </dl>                                                         | Nota al pie de página de una página de un documento.<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**AnnotationType \_ FormatChange**</dt> <dt>60014</dt> </dl>                                         | Cambio de formato que se realizó.<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**AnnotationType \_ FormulaError**</dt> <dt>60004</dt> </dl>                                         | Error en una fórmula. Los errores de fórmula suelen incluir texto rojo y signos de exclamación.<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**AnnotationType \_ GrammarError**</dt> <dt>60002</dt> </dl>                                         | Un error gramatical, a menudo indicado por una línea ondulada de color verde. <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**AnnotationType \_ Encabezado**</dt> <dt>60006</dt> </dl>                                                                 | Encabezado de una página de un documento.<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**AnnotationType \_ Resaltado**</dt> <dt>60008</dt> </dl>                                             | Contenido resaltado, normalmente indicado por un color de fondo de contraste.<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**AnnotationType \_ InsertionChange**</dt> <dt>60011</dt> </dl>                             | Cambio de inserción realizado en el documento.<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**AnnotationType \_ Matemáticas**</dt> <dt>60023</dt> </dl>                                             | Intervalo de texto que contiene matemáticas.<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**AnnotationType \_ MoveChange**</dt> <dt>60013</dt> </dl>                                                 | Cambio de movimiento realizado en el documento.<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**AnnotationType \_ SpellingError**</dt> <dt>60001</dt> </dl>                                     | Un error ortográfico, normalmente indicado por una línea ondulada de color rojo. <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**AnnotationType \_ TrackChanges**</dt> <dt>60005</dt> </dl>                                         | Cambio que se realizó en el documento.<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**AnnotationType \_ Desconocido**</dt> <dt>60000</dt> </dl>                                                             | No se conoce el tipo de anotación.<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**AnnotationType \_ UnsyncedChange**</dt> <dt>60015</dt> </dl>                                 | Cambio no sincronizado realizado en el documento.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                            |
| Encabezado<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**IAnnotationProvider::AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**IUIAutomationPattern::CachedAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**IUIAutomationPattern::CurrentAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**Vista**
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

